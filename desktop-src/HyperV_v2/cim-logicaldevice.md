---
description: Eine Abstraktion oder Emulation einer Hardware Entität, die auf physischer Hardware basieren kann oder nicht.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749656"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="0d9dc-103">CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="0d9dc-104">Eine Abstraktion oder Emulation einer Hardware Entität, die auf physischer Hardware basieren kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d9dc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="0d9dc-106">Member</span><span class="sxs-lookup"><span data-stu-id="0d9dc-106">Members</span></span>

<span data-ttu-id="0d9dc-107">Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0d9dc-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="0d9dc-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0d9dc-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d9dc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d9dc-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d9dc-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0d9dc-110">Methods</span></span>

<span data-ttu-id="0d9dc-111">Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="0d9dc-112">Methode</span><span class="sxs-lookup"><span data-stu-id="0d9dc-112">Method</span></span>                                                           | <span data-ttu-id="0d9dc-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d9dc-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d9dc-114">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="0d9dc-115">Diese Methode ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-115">This method is deprecated.</span></span> <span data-ttu-id="0d9dc-116">Verwenden Sie stattdessen die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="0d9dc-117">**Veraltete Beschreibung:** Aktiviert oder deaktiviert das logische Gerät.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="0d9dc-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="0d9dc-119">Diese Methode ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-119">This method is deprecated.</span></span> <span data-ttu-id="0d9dc-120">Verwenden Sie stattdessen die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="0d9dc-121">**Veraltete Beschreibung:** Schaltet das logische Gerät online, damit es Anforderungen akzeptieren oder offline schalten kann, sodass keine Anforderungen mehr akzeptiert werden können.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="0d9dc-122">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="0d9dc-123">Diese Methode ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-123">This method is deprecated.</span></span> <span data-ttu-id="0d9dc-124">Verwenden Sie stattdessen die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="0d9dc-125">**Veraltete Beschreibung:** Hält die Aktivität vorübergehend auf dem logischen Gerät an oder aktiviert die Aktivität erneut.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="0d9dc-126">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="0d9dc-127">Setzt das logische Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="0d9dc-128">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="0d9dc-129">Stellt eine vorherige Konfiguration und den Status des logischen Geräts wieder her.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="0d9dc-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="0d9dc-131">Speichert die Konfiguration und den Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="0d9dc-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="0d9dc-133">Diese Methode ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-133">This method is deprecated.</span></span> <span data-ttu-id="0d9dc-134">Verwenden Sie stattdessen die **SetPowerState** -Eigenschaft der **CIM- \_ powermanagementservice** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="0d9dc-135">**Veraltete Beschreibung:** Legt den Energiezustand des logischen Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="0d9dc-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d9dc-136">Properties</span></span>

<span data-ttu-id="0d9dc-137">Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d9dc-138">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-139">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0d9dc-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-141">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Verfügbarkeit**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-142">Ein Array, das neben dem der **Verfügbarkeits** Eigenschaft Verfügbarkeitsinformationen über das logische Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d9dc-143">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d9dc-144">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0d9dc-145">**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0d9dc-146">**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0d9dc-147">**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d9dc-148">**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0d9dc-149">**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0d9dc-150">**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0d9dc-151">**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d9dc-152">Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="0d9dc-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0d9dc-153">**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0d9dc-154">**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0d9dc-155">**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0d9dc-156">**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0d9dc-157">**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0d9dc-158">**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0d9dc-159">**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0d9dc-160">**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0d9dc-161">**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0d9dc-162">**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0d9dc-163">Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="0d9dc-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d9dc-164">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-167">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 006,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus "," MIF. DMTF- \| Host Gerät \| 001,5 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Additionalavailability**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-168">Enthält die Verfügbarkeit des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d9dc-169">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d9dc-170">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0d9dc-171">**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0d9dc-172">**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0d9dc-173">**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d9dc-174">**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0d9dc-175">**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0d9dc-176">**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0d9dc-177">**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d9dc-178">Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="0d9dc-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0d9dc-179">**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0d9dc-180">**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0d9dc-181">**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0d9dc-182">**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0d9dc-183">**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0d9dc-184">**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0d9dc-185">**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0d9dc-186">**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0d9dc-187">**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0d9dc-188">**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0d9dc-189">Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="0d9dc-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d9dc-190">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-193">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-194">Der Klassenname, der zum Erstellen einer Instanz des logischen Geräts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="0d9dc-195">" **Kreationclassname** " wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-199">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-200">Ein eindeutiger Bezeichner des logischen Geräts, z. b. die Adresse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-201">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-202">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0d9dc-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-204">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)".**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-205">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-205">This property is deprecated.</span></span> <span data-ttu-id="0d9dc-206">Verwenden Sie stattdessen die Eigenschaft **OperationalStatus** aus der **CIM \_ ManagedSystemElement** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="0d9dc-207">**Veraltete Beschreibung:** Gibt an, ob ein von der **LastErrorCode** -Eigenschaft gemeldeter Fehler gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-211">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ deviceerrordata. ErrorDescription")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-212">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-212">This property is deprecated.</span></span> <span data-ttu-id="0d9dc-213">Verwenden Sie stattdessen die **ErrorDescription** -Eigenschaft aus der **CIM \_ deviceerrordata** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="0d9dc-214">**Veraltete Beschreibung:** Zusätzliche Informationen über den Fehler, der von der **LastErrorCode** -Eigenschaft gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-216">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0d9dc-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-218">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**"OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-219">Ein Array von Zeichen folgen, die die " **OtherIdentifyingInfo** "-Array Elemente desselben Indexes beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-220">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-221">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-223">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ deviceerrordata. LastErrorCode")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-224">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-224">This property is deprecated.</span></span> <span data-ttu-id="0d9dc-225">Stattdessen verwenden wir die Eigenschaft " **LastErrorCode** " aus der **CIM \_ deviceerrordata** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="0d9dc-226">**Veraltete Beschreibung:** Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-227">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-228">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-230">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-231">Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="0d9dc-232">**Veraltete Beschreibung:** Die maximale Zeit in Millisekunden, die ein Gerät in einem temporär deaktivierten Zustand verbleiben kann (**Availability** und **additionalavailability** -Eigenschaften sind auf "21" festgelegt).</span><span class="sxs-lookup"><span data-stu-id="0d9dc-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="0d9dc-233">Der Wert "0" gibt an, dass das logische Gerät unbegrenzt in einem temporär deaktivierten Zustand bleiben kann.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-235">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0d9dc-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-237">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Identifyingbeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-238">Informationen, die das logische Gerät außer der **DeviceID** identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-239">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-240">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0d9dc-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-242">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ powermanagementfunktionalitäten. Power-Funktionen")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-243">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-243">This property is deprecated.</span></span> <span data-ttu-id="0d9dc-244">Verwenden Sie stattdessen die **CIM- \_ powermanagementfunktionalitäten** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="0d9dc-245">**Veraltete Beschreibung:** Ein Array, das die Energie Verwaltungsfunktionen des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d9dc-246">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0d9dc-247">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d9dc-248">**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d9dc-249">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0d9dc-250">**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0d9dc-251">**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0d9dc-252">**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0d9dc-253">**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d9dc-254">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-255">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0d9dc-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-257">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ powermanagementfunktionalitäten")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-258">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-258">This property is deprecated.</span></span> <span data-ttu-id="0d9dc-259">Verwenden Sie stattdessen die **powermanagementfunktionalitäten** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="0d9dc-260">**Veraltete Beschreibung: true** , wenn das logische Gerät Energie gesteuert werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-261">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-262">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-264">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stunden"), **Counter**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-265">Die Anzahl der aufeinanderfolgenden Stunden, die das logische Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-269">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md).**Enabledstate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". \|Betriebsstatus DMTF \| 006,4 ")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-270">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-270">This property is deprecated.</span></span> <span data-ttu-id="0d9dc-271">Verwenden Sie stattdessen die **CIM- \_ powermanagementfunktionalitäten** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="0d9dc-272">**Veraltete Beschreibung:** Gibt an, ob das logische Gerät aktiviert ist oder sich in einem verknüpften Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d9dc-273">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d9dc-274">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d9dc-275">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d9dc-276">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d9dc-277">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d9dc-278">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-281">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-282">Der Klassenname, der zum Erstellen einer Instanz des Systems verwendet wird, das das logische Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="0d9dc-283">**Systemkreationclassname** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-284">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-287">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="0d9dc-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-288">Der Name des Systems, das das logische Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="0d9dc-289">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9dc-290">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d9dc-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9dc-292">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stunden"), **Counter**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="0d9dc-293">Die Gesamtzahl der Stunden, die das logische Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="0d9dc-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d9dc-294">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d9dc-294">Requirements</span></span>



| <span data-ttu-id="0d9dc-295">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d9dc-295">Requirement</span></span> | <span data-ttu-id="0d9dc-296">Wert</span><span class="sxs-lookup"><span data-stu-id="0d9dc-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9dc-297">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-297">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9dc-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0d9dc-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0d9dc-299">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d9dc-299">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9dc-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d9dc-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0d9dc-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d9dc-301">Namespace</span></span><br/>                | <span data-ttu-id="0d9dc-302">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d9dc-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d9dc-303">MOF</span><span class="sxs-lookup"><span data-stu-id="0d9dc-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d9dc-304"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d9dc-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d9dc-305">DLL</span><span class="sxs-lookup"><span data-stu-id="0d9dc-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d9dc-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d9dc-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d9dc-307">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d9dc-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9dc-308">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="0d9dc-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

