---
description: Die Win32- \_ Parallelport-&\# 32; Die WMI-Klasse stellt die Eigenschaften eines parallelen Ports auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 986bd27f-71b0-4a40-a421-a8bfc0f081be
ms.tgt_platform: multiple
title: Win32_ParallelPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ParallelPort
- Win32_ParallelPort.Reset
- Win32_ParallelPort.SetPowerState
- Win32_ParallelPort.Availability
- Win32_ParallelPort.Capabilities
- Win32_ParallelPort.CapabilityDescriptions
- Win32_ParallelPort.Caption
- Win32_ParallelPort.ConfigManagerErrorCode
- Win32_ParallelPort.ConfigManagerUserConfig
- Win32_ParallelPort.CreationClassName
- Win32_ParallelPort.Description
- Win32_ParallelPort.DeviceID
- Win32_ParallelPort.DMASupport
- Win32_ParallelPort.ErrorCleared
- Win32_ParallelPort.ErrorDescription
- Win32_ParallelPort.InstallDate
- Win32_ParallelPort.LastErrorCode
- Win32_ParallelPort.MaxNumberControlled
- Win32_ParallelPort.Name
- Win32_ParallelPort.OSAutoDiscovered
- Win32_ParallelPort.PNPDeviceID
- Win32_ParallelPort.PowerManagementCapabilities
- Win32_ParallelPort.PowerManagementSupported
- Win32_ParallelPort.ProtocolSupported
- Win32_ParallelPort.Status
- Win32_ParallelPort.StatusInfo
- Win32_ParallelPort.SystemCreationClassName
- Win32_ParallelPort.SystemName
- Win32_ParallelPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da2ed3b34f3655067fd5ae41c31424e7599789c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127456"
---
# <a name="win32_parallelport-class"></a><span data-ttu-id="2794e-103">Win32 \_ Parallelport-Klasse</span><span class="sxs-lookup"><span data-stu-id="2794e-103">Win32\_ParallelPort class</span></span>

<span data-ttu-id="2794e-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Parallelport** stellt die Eigenschaften eines parallelen Ports auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2794e-104">The **Win32\_ParallelPort** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a parallel port on a computer system running Windows.</span></span>

<span data-ttu-id="2794e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2794e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2794e-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2794e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2794e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2794e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class  Win32_ParallelPort : CIM_ParallelController
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="2794e-108">Member</span><span class="sxs-lookup"><span data-stu-id="2794e-108">Members</span></span>

<span data-ttu-id="2794e-109">Die **Win32- \_ Parallelport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2794e-109">The **Win32\_ParallelPort** class has these types of members:</span></span>

-   [<span data-ttu-id="2794e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="2794e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2794e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2794e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2794e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="2794e-112">Methods</span></span>

<span data-ttu-id="2794e-113">Die **Win32- \_ Parallelport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2794e-113">The **Win32\_ParallelPort** class has these methods.</span></span>



| <span data-ttu-id="2794e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="2794e-114">Method</span></span>            | <span data-ttu-id="2794e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2794e-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2794e-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="2794e-116">**Reset**</span></span>         | <span data-ttu-id="2794e-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2794e-117">Not implemented.</span></span> <span data-ttu-id="2794e-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ parallelcontroller**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="2794e-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="2794e-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2794e-119">**SetPowerState**</span></span> | <span data-ttu-id="2794e-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2794e-120">Not implemented.</span></span> <span data-ttu-id="2794e-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ parallelcontroller**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="2794e-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2794e-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2794e-122">Properties</span></span>

<span data-ttu-id="2794e-123">Die **Win32- \_ Parallelport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2794e-123">The **Win32\_ParallelPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2794e-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="2794e-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2794e-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-127">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="2794e-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2794e-128">Availability and status of the device.</span></span>

<span data-ttu-id="2794e-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2794e-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2794e-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2794e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2794e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2794e-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="2794e-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="2794e-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2794e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="2794e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2794e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="2794e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2794e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="2794e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2794e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="2794e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2794e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="2794e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2794e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="2794e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2794e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="2794e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2794e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="2794e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2794e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="2794e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2794e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="2794e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="2794e-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2794e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="2794e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2794e-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2794e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="2794e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2794e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="2794e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2794e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="2794e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="2794e-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2794e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="2794e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="2794e-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2794e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="2794e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="2794e-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2794e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="2794e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2794e-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2794e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="2794e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="2794e-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-160">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2794e-160">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-161">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2794e-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2794e-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-163">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Parallele Ports \| 003,8 "), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ parallelcontroller**](cim-parallelcontroller.md)".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="2794e-163">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-164">Array der Funktionen des parallelen Controllers.</span><span class="sxs-lookup"><span data-stu-id="2794e-164">Array of the capabilities of the parallel controller.</span></span>

<span data-ttu-id="2794e-165">Diese Eigenschaft wird von [**CIM \_ parallelcontroller**](cim-parallelcontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-165">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2794e-166">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2794e-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2794e-167">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2794e-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="2794e-168">**XT/kompatibel** (2)</span><span class="sxs-lookup"><span data-stu-id="2794e-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="2794e-169">**PS/2-kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="2794e-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="2794e-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="2794e-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="2794e-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="2794e-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="2794e-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="2794e-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="2794e-173">**PC-98-hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="2794e-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="2794e-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="2794e-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-175">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="2794e-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-176">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2794e-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2794e-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-178">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ parallelcontroller**](cim-parallelcontroller.md)".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="2794e-178">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-179">Array ausführlicherer Erläuterungen für alle parallelen Controller Features, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="2794e-179">Array of more detailed explanations for any of the parallel controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="2794e-180">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="2794e-180">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="2794e-181">Diese Eigenschaft wird von [**CIM \_ parallelcontroller**](cim-parallelcontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-181">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2794e-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-185">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2794e-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-186">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2794e-186">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="2794e-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-188">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="2794e-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-189">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2794e-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-191">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2794e-191">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-192">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2794e-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2794e-193">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2794e-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="2794e-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2794e-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="2794e-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-196">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2794e-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2794e-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="2794e-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2794e-198">(1)</span><span class="sxs-lookup"><span data-stu-id="2794e-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-199">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2794e-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2794e-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="2794e-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2794e-201">(2)</span><span class="sxs-lookup"><span data-stu-id="2794e-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2794e-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="2794e-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2794e-203">(3)</span><span class="sxs-lookup"><span data-stu-id="2794e-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-204">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2794e-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2794e-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="2794e-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2794e-206">(4)</span><span class="sxs-lookup"><span data-stu-id="2794e-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-207">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2794e-207">Device is not working properly.</span></span> <span data-ttu-id="2794e-208">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="2794e-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2794e-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="2794e-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2794e-210">(5)</span><span class="sxs-lookup"><span data-stu-id="2794e-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-211">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2794e-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2794e-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="2794e-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2794e-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="2794e-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-214">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="2794e-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2794e-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="2794e-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2794e-216">(7)</span><span class="sxs-lookup"><span data-stu-id="2794e-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2794e-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="2794e-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2794e-218">(8)</span><span class="sxs-lookup"><span data-stu-id="2794e-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-219">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="2794e-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2794e-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="2794e-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2794e-221">(9)</span><span class="sxs-lookup"><span data-stu-id="2794e-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-222">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2794e-222">Device is not working properly.</span></span> <span data-ttu-id="2794e-223">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="2794e-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2794e-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="2794e-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2794e-225">(10)</span><span class="sxs-lookup"><span data-stu-id="2794e-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-226">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2794e-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="2794e-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2794e-228">(11)</span><span class="sxs-lookup"><span data-stu-id="2794e-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-229">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="2794e-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2794e-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="2794e-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2794e-231">(12)</span><span class="sxs-lookup"><span data-stu-id="2794e-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-232">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="2794e-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2794e-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="2794e-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2794e-234">(13)</span><span class="sxs-lookup"><span data-stu-id="2794e-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-235">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2794e-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="2794e-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2794e-237">(14)</span><span class="sxs-lookup"><span data-stu-id="2794e-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-238">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2794e-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2794e-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="2794e-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2794e-240">(15)</span><span class="sxs-lookup"><span data-stu-id="2794e-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-241">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2794e-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2794e-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="2794e-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2794e-243">(16)</span><span class="sxs-lookup"><span data-stu-id="2794e-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-244">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2794e-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="2794e-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2794e-246">(17)</span><span class="sxs-lookup"><span data-stu-id="2794e-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-247">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="2794e-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2794e-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="2794e-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2794e-249">(18)</span><span class="sxs-lookup"><span data-stu-id="2794e-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-250">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2794e-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="2794e-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2794e-252">(19)</span><span class="sxs-lookup"><span data-stu-id="2794e-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2794e-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="2794e-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2794e-254">(20)</span><span class="sxs-lookup"><span data-stu-id="2794e-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-255">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="2794e-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2794e-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="2794e-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2794e-257">(21)</span><span class="sxs-lookup"><span data-stu-id="2794e-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-258">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="2794e-258">System failure.</span></span> <span data-ttu-id="2794e-259">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2794e-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2794e-260">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="2794e-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2794e-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="2794e-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2794e-262">(22)</span><span class="sxs-lookup"><span data-stu-id="2794e-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-263">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2794e-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2794e-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="2794e-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2794e-265">(23)</span><span class="sxs-lookup"><span data-stu-id="2794e-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-266">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="2794e-266">System failure.</span></span> <span data-ttu-id="2794e-267">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2794e-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2794e-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="2794e-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2794e-269">(24)</span><span class="sxs-lookup"><span data-stu-id="2794e-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-270">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="2794e-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2794e-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="2794e-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2794e-272">(25)</span><span class="sxs-lookup"><span data-stu-id="2794e-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-273">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="2794e-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2794e-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="2794e-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2794e-275">(26)</span><span class="sxs-lookup"><span data-stu-id="2794e-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-276">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="2794e-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2794e-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="2794e-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2794e-278">(27)</span><span class="sxs-lookup"><span data-stu-id="2794e-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-279">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2794e-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2794e-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="2794e-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2794e-281">(28)</span><span class="sxs-lookup"><span data-stu-id="2794e-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-282">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="2794e-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2794e-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="2794e-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2794e-284">(29)</span><span class="sxs-lookup"><span data-stu-id="2794e-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-285">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2794e-285">Device is disabled.</span></span> <span data-ttu-id="2794e-286">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2794e-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2794e-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="2794e-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2794e-288">(30)</span><span class="sxs-lookup"><span data-stu-id="2794e-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-289">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2794e-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2794e-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="2794e-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2794e-291">31,5</span><span class="sxs-lookup"><span data-stu-id="2794e-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-292">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2794e-292">Device is not working properly.</span></span> <span data-ttu-id="2794e-293">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-294">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="2794e-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-295">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2794e-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-297">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2794e-297">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-298">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="2794e-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2794e-299">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-300">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="2794e-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-303">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2794e-303">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2794e-304">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2794e-304">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2794e-305">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-305">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="2794e-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-307">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2794e-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-310">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2794e-310">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-311">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2794e-311">Description of the object.</span></span>

<span data-ttu-id="2794e-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2794e-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-316">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2794e-316">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-317">Der Bezeichner des parallelen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="2794e-317">Identifier of the parallel port.</span></span>

<span data-ttu-id="2794e-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-319">**Dmasupport**</span><span class="sxs-lookup"><span data-stu-id="2794e-319">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-320">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2794e-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-322">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Parallele Ports \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="2794e-322">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-323">**True** gibt an, dass der parallele Port DMA unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2794e-323">If **TRUE**, the parallel port supports DMA.</span></span>

<span data-ttu-id="2794e-324">Diese Eigenschaft wird von [**CIM \_ parallelcontroller**](cim-parallelcontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-324">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-325">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="2794e-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-326">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2794e-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2794e-328">Wenn der Wert **true** ist, wird der in **LastErrorCode** gemeldete Fehler gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2794e-328">If **TRUE**, the error reported in **LastErrorCode** is cleared.</span></span>

<span data-ttu-id="2794e-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2794e-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2794e-333">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu Maßnahmen, die möglicherweise durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-333">More information about the error recorded in **LastErrorCode**, and information about corrective actions that might be taken.</span></span>

<span data-ttu-id="2794e-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2794e-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-336">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2794e-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-338">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="2794e-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-339">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2794e-339">Date and time the object was installed.</span></span> <span data-ttu-id="2794e-340">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2794e-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2794e-341">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2794e-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-343">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2794e-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2794e-345">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2794e-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2794e-346">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-347">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="2794e-347">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-348">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2794e-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-350">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="2794e-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-351">Maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-351">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="2794e-352">Wenn die Zahl unbekannt ist, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-352">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="2794e-353">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-353">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-354">**Name**</span><span class="sxs-lookup"><span data-stu-id="2794e-354">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-357">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2794e-357">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-358">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2794e-358">Label by which the object is known.</span></span> <span data-ttu-id="2794e-359">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-359">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2794e-360">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-360">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-361">**Osauum erkannt**</span><span class="sxs-lookup"><span data-stu-id="2794e-361">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-362">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2794e-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-364">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2794e-364">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-365">**True** gibt an, dass der parallele Port vom Betriebssystem automatisch erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="2794e-365">If **TRUE**, the parallel port was automatically detected by the operating system.</span></span> <span data-ttu-id="2794e-366">**False** gibt an, dass der Port auf andere Weise erkannt wurde (z. b. manuell über die Systemsteuerung hinzugefügt).</span><span class="sxs-lookup"><span data-stu-id="2794e-366">If **FALSE**, the port was detected by other means (such as being manually added through the Control Panel).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-367">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2794e-367">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-368">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-370">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2794e-370">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-371">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2794e-371">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2794e-372">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2794e-373">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2794e-373">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2794e-374">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="2794e-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-375">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2794e-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2794e-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2794e-377">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2794e-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2794e-378">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2794e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2794e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2794e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2794e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2794e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="2794e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2794e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="2794e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-383">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2794e-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2794e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="2794e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-385">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="2794e-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2794e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="2794e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-387">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2794e-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2794e-388">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2794e-389">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="2794e-389">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2794e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="2794e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-391">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2794e-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2794e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="2794e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2794e-393">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="2794e-393">Timed Power-On Supported</span></span>

<span data-ttu-id="2794e-394">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2794e-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-395">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="2794e-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-396">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2794e-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2794e-398">**True** gibt an, dass das Gerät Energie gesteuert werden kann. Dies bedeutet, dass es in den Unterbrechungs Modus versetzt werden kann usw.</span><span class="sxs-lookup"><span data-stu-id="2794e-398">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="2794e-399">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="2794e-399">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="2794e-400">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-401">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="2794e-401">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-402">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2794e-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-404">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2794e-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-405">Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2794e-405">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="2794e-406">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-406">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="2794e-407">Werte werden in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2794e-407">Values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2794e-408">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2794e-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2794e-409">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2794e-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="2794e-410">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="2794e-410">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="2794e-411">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="2794e-411">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="2794e-412">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="2794e-412">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="2794e-413">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="2794e-413">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="2794e-414">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="2794e-414">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="2794e-415">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="2794e-415">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="2794e-416">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="2794e-416">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="2794e-417">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="2794e-417">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="2794e-418">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="2794e-418">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="2794e-419">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="2794e-419">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="2794e-420">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="2794e-420">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="2794e-421">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="2794e-421">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="2794e-422">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="2794e-422">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="2794e-423">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="2794e-423">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="2794e-424">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="2794e-424">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="2794e-425">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="2794e-425">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="2794e-426">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="2794e-426">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="2794e-427">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="2794e-427">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="2794e-428">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="2794e-428">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="2794e-429">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="2794e-429">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="2794e-430">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="2794e-430">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="2794e-431">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="2794e-431">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="2794e-432">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="2794e-432">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="2794e-433">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="2794e-433">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="2794e-434">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="2794e-434">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="2794e-435">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="2794e-435">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="2794e-436">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="2794e-436">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="2794e-437">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="2794e-437">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="2794e-438">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="2794e-438">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="2794e-439">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="2794e-439">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="2794e-440">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="2794e-440">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="2794e-441">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="2794e-441">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="2794e-442">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="2794e-442">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="2794e-443">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="2794e-443">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="2794e-444">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="2794e-444">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="2794e-445">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="2794e-445">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="2794e-446">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="2794e-446">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="2794e-447">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="2794e-447">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="2794e-448">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="2794e-448">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="2794e-449">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="2794e-449">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="2794e-450">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="2794e-450">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="2794e-451">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="2794e-451">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="2794e-452">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="2794e-452">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="2794e-453">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="2794e-453">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="2794e-454">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="2794e-454">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-455">**Status**</span><span class="sxs-lookup"><span data-stu-id="2794e-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-456">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-458">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2794e-458">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-459">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2794e-459">Current status of the object.</span></span> <span data-ttu-id="2794e-460">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2794e-461">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="2794e-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2794e-462">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="2794e-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2794e-463">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-463">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2794e-464">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="2794e-464">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2794e-465">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2794e-466">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="2794e-466">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2794e-467">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2794e-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2794e-468">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="2794e-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2794e-469">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="2794e-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2794e-470">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="2794e-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2794e-471">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2794e-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2794e-472">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="2794e-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2794e-473">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="2794e-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2794e-474">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="2794e-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2794e-475">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="2794e-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2794e-476">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="2794e-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2794e-477">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="2794e-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2794e-478">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="2794e-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2794e-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-480">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2794e-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-482">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2794e-482">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2794e-483">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2794e-483">State of the logical device.</span></span> <span data-ttu-id="2794e-484">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2794e-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2794e-485">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2794e-486">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2794e-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2794e-487">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2794e-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2794e-488">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="2794e-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2794e-489">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="2794e-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2794e-490">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="2794e-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2794e-491">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="2794e-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-492">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-494">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2794e-494">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2794e-495">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="2794e-495">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="2794e-496">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-496">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-497">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="2794e-497">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-498">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2794e-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2794e-500">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2794e-500">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2794e-501">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2794e-501">Name of the scoping system.</span></span>

<span data-ttu-id="2794e-502">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2794e-503">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="2794e-503">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2794e-504">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2794e-504">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2794e-505">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2794e-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2794e-506">Datum und Uhrzeit der letzten zurück setzung des Controllers.</span><span class="sxs-lookup"><span data-stu-id="2794e-506">Date and time the controller was last reset.</span></span> <span data-ttu-id="2794e-507">Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2794e-507">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="2794e-508">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2794e-508">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2794e-509">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2794e-509">Remarks</span></span>

<span data-ttu-id="2794e-510">Die **Win32- \_ Parallelport** -Klasse wird von [**CIM \_ parallelcontroller**](cim-parallelcontroller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2794e-510">The **Win32\_ParallelPort** class is derived from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2794e-511">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2794e-511">Requirements</span></span>



| <span data-ttu-id="2794e-512">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2794e-512">Requirement</span></span> | <span data-ttu-id="2794e-513">Wert</span><span class="sxs-lookup"><span data-stu-id="2794e-513">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2794e-514">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2794e-514">Minimum supported client</span></span><br/> | <span data-ttu-id="2794e-515">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2794e-515">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2794e-516">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2794e-516">Minimum supported server</span></span><br/> | <span data-ttu-id="2794e-517">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2794e-517">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2794e-518">Namespace</span><span class="sxs-lookup"><span data-stu-id="2794e-518">Namespace</span></span><br/>                | <span data-ttu-id="2794e-519">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2794e-519">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2794e-520">MOF</span><span class="sxs-lookup"><span data-stu-id="2794e-520">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2794e-521"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2794e-521"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2794e-522">DLL</span><span class="sxs-lookup"><span data-stu-id="2794e-522">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2794e-523"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2794e-523"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2794e-524">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2794e-524">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2794e-525">**CIM- \_ parallelcontroller**</span><span class="sxs-lookup"><span data-stu-id="2794e-525">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dt>

[<span data-ttu-id="2794e-526">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="2794e-526">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
