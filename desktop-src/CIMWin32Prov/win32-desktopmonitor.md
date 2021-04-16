---
description: Stellt den Typ des Monitors oder des Anzeige Geräts dar, das mit dem Computersystem verbunden ist.
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Win32_DesktopMonitor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524291"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="7fd35-103">Win32 \_ Desktopmonitor-Klasse</span><span class="sxs-lookup"><span data-stu-id="7fd35-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="7fd35-104">Die **Win32 \_ Desktopmonitor** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt den Monitortyp oder das Anzeigegerät dar, das mit dem Computersystem verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="7fd35-105">Hardware, die nicht mit dem Windows-Anzeigetreiber Modell (WDDM) kompatibel ist, gibt falsche Eigenschaftswerte für Instanzen dieser Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd35-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="7fd35-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fd35-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7fd35-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7fd35-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd35-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fd35-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="7fd35-109">Member</span><span class="sxs-lookup"><span data-stu-id="7fd35-109">Members</span></span>

<span data-ttu-id="7fd35-110">Die **Win32 \_ Desktopmonitor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7fd35-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="7fd35-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7fd35-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7fd35-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fd35-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7fd35-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="7fd35-113">Methods</span></span>

<span data-ttu-id="7fd35-114">Die **Win32 \_ Desktopmonitor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="7fd35-115">Methode</span><span class="sxs-lookup"><span data-stu-id="7fd35-115">Method</span></span>            | <span data-ttu-id="7fd35-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fd35-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd35-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="7fd35-117">**Reset**</span></span>         | <span data-ttu-id="7fd35-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-118">Not implemented.</span></span> <span data-ttu-id="7fd35-119">Informationen zur Implementierung dieser Methode finden Sie in der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd35-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="7fd35-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7fd35-120">**SetPowerState**</span></span> | <span data-ttu-id="7fd35-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-121">Not implemented.</span></span> <span data-ttu-id="7fd35-122">Informationen zur Implementierung dieser Methode finden Sie in der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd35-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7fd35-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fd35-123">Properties</span></span>

<span data-ttu-id="7fd35-124">Die **Win32 \_ Desktopmonitor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fd35-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fd35-125">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="7fd35-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fd35-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="7fd35-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-129">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-129">Availability and status of the device.</span></span>

<span data-ttu-id="7fd35-130">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7fd35-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7fd35-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fd35-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7fd35-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7fd35-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="7fd35-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-134">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="7fd35-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7fd35-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="7fd35-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7fd35-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="7fd35-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7fd35-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="7fd35-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7fd35-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="7fd35-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7fd35-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="7fd35-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7fd35-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="7fd35-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7fd35-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="7fd35-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7fd35-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="7fd35-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7fd35-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="7fd35-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7fd35-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="7fd35-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7fd35-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="7fd35-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7fd35-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="7fd35-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7fd35-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="7fd35-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7fd35-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="7fd35-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="7fd35-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7fd35-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="7fd35-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="7fd35-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7fd35-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="7fd35-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="7fd35-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7fd35-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="7fd35-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7fd35-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="7fd35-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="7fd35-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd35-161">**Bandwidth**</span><span class="sxs-lookup"><span data-stu-id="7fd35-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-164">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz")</span><span class="sxs-lookup"><span data-stu-id="7fd35-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-165">Überwachen der Bandbreite in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="7fd35-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="7fd35-166">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="7fd35-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="7fd35-167">Diese Eigenschaft wird von [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7fd35-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-171">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7fd35-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-172">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-172">Short description of the object.</span></span>

<span data-ttu-id="7fd35-173">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-174">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="7fd35-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-175">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-177">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7fd35-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-178">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7fd35-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7fd35-179">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7fd35-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7fd35-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="7fd35-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-182">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7fd35-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7fd35-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7fd35-184">(1)</span><span class="sxs-lookup"><span data-stu-id="7fd35-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-185">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7fd35-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7fd35-187">(2)</span><span class="sxs-lookup"><span data-stu-id="7fd35-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7fd35-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7fd35-189">(3)</span><span class="sxs-lookup"><span data-stu-id="7fd35-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-190">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7fd35-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7fd35-192">(4)</span><span class="sxs-lookup"><span data-stu-id="7fd35-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-193">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7fd35-193">Device is not working properly.</span></span> <span data-ttu-id="7fd35-194">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7fd35-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7fd35-196">(5)</span><span class="sxs-lookup"><span data-stu-id="7fd35-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-197">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fd35-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7fd35-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7fd35-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="7fd35-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-200">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="7fd35-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7fd35-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7fd35-202">(7)</span><span class="sxs-lookup"><span data-stu-id="7fd35-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7fd35-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7fd35-204">(8)</span><span class="sxs-lookup"><span data-stu-id="7fd35-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-205">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7fd35-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7fd35-207">(9)</span><span class="sxs-lookup"><span data-stu-id="7fd35-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-208">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7fd35-208">Device is not working properly.</span></span> <span data-ttu-id="7fd35-209">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="7fd35-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7fd35-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7fd35-211">(10)</span><span class="sxs-lookup"><span data-stu-id="7fd35-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-212">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7fd35-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7fd35-214">(11)</span><span class="sxs-lookup"><span data-stu-id="7fd35-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-215">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="7fd35-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7fd35-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7fd35-217">(12)</span><span class="sxs-lookup"><span data-stu-id="7fd35-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-218">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7fd35-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7fd35-220">(13)</span><span class="sxs-lookup"><span data-stu-id="7fd35-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-221">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7fd35-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7fd35-223">(14)</span><span class="sxs-lookup"><span data-stu-id="7fd35-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-224">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7fd35-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7fd35-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7fd35-226">(15)</span><span class="sxs-lookup"><span data-stu-id="7fd35-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-227">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7fd35-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7fd35-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7fd35-229">(16)</span><span class="sxs-lookup"><span data-stu-id="7fd35-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-230">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7fd35-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7fd35-232">(17)</span><span class="sxs-lookup"><span data-stu-id="7fd35-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-233">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="7fd35-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7fd35-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7fd35-235">(18)</span><span class="sxs-lookup"><span data-stu-id="7fd35-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-236">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7fd35-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7fd35-238">(19)</span><span class="sxs-lookup"><span data-stu-id="7fd35-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7fd35-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7fd35-240">(20)</span><span class="sxs-lookup"><span data-stu-id="7fd35-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-241">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7fd35-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7fd35-243">(21)</span><span class="sxs-lookup"><span data-stu-id="7fd35-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="7fd35-244">System failure.</span></span> <span data-ttu-id="7fd35-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7fd35-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7fd35-246">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7fd35-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7fd35-248">(22)</span><span class="sxs-lookup"><span data-stu-id="7fd35-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-249">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7fd35-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7fd35-251">(23)</span><span class="sxs-lookup"><span data-stu-id="7fd35-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-252">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="7fd35-252">System failure.</span></span> <span data-ttu-id="7fd35-253">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7fd35-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7fd35-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7fd35-255">(24)</span><span class="sxs-lookup"><span data-stu-id="7fd35-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-256">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7fd35-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7fd35-258">(25)</span><span class="sxs-lookup"><span data-stu-id="7fd35-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-259">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="7fd35-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7fd35-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7fd35-261">(26)</span><span class="sxs-lookup"><span data-stu-id="7fd35-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-262">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="7fd35-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7fd35-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7fd35-264">(27)</span><span class="sxs-lookup"><span data-stu-id="7fd35-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-265">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fd35-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7fd35-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7fd35-267">(28)</span><span class="sxs-lookup"><span data-stu-id="7fd35-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-268">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7fd35-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7fd35-270">(29)</span><span class="sxs-lookup"><span data-stu-id="7fd35-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-271">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-271">Device is disabled.</span></span> <span data-ttu-id="7fd35-272">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7fd35-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7fd35-274">(30)</span><span class="sxs-lookup"><span data-stu-id="7fd35-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-275">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fd35-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7fd35-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="7fd35-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7fd35-277">31,5</span><span class="sxs-lookup"><span data-stu-id="7fd35-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-278">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7fd35-278">Device is not working properly.</span></span> <span data-ttu-id="7fd35-279">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd35-280">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="7fd35-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-281">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7fd35-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-283">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7fd35-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-284">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fd35-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7fd35-285">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-286">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7fd35-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-289">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7fd35-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-290">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fd35-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7fd35-291">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7fd35-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-293">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fd35-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-296">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7fd35-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-297">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-297">Description of the object.</span></span>

<span data-ttu-id="7fd35-298">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-299">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7fd35-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-302">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows GDI \| Hmonitor")</span><span class="sxs-lookup"><span data-stu-id="7fd35-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-303">Eindeutiger Bezeichner eines Desktop Monitors.</span><span class="sxs-lookup"><span data-stu-id="7fd35-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="7fd35-304">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-305">**Display Type**</span><span class="sxs-lookup"><span data-stu-id="7fd35-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-306">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fd35-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-308">Typ des Desktop Monitors oder der CRT.</span><span class="sxs-lookup"><span data-stu-id="7fd35-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="7fd35-309">Diese Eigenschaft wird von [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fd35-310">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7fd35-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7fd35-311">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7fd35-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="7fd35-312">**MultiScan-Farbe** (2)</span><span class="sxs-lookup"><span data-stu-id="7fd35-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="7fd35-313">**MultiScan-monochrome** (3)</span><span class="sxs-lookup"><span data-stu-id="7fd35-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="7fd35-314">**Farbe für fixierte Häufigkeit** (4)</span><span class="sxs-lookup"><span data-stu-id="7fd35-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="7fd35-315">**Fester Frequenz-Mono** (5)</span><span class="sxs-lookup"><span data-stu-id="7fd35-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd35-316">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="7fd35-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-317">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7fd35-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-319">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7fd35-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7fd35-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7fd35-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-324">Eine frei Form Zeichenfolge, die weitere Informationen über den in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="7fd35-325">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7fd35-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-327">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fd35-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-329">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7fd35-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-330">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-330">Date and time the object was installed.</span></span> <span data-ttu-id="7fd35-331">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7fd35-332">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="7fd35-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-334">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7fd35-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-336">**True** gibt an, dass das Gerät gesperrt ist und Benutzereingaben oder-Ausgaben verhindert.</span><span class="sxs-lookup"><span data-stu-id="7fd35-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="7fd35-337">Diese Eigenschaft wird von [**CIM \_ userdevice**](cim-userdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-338">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7fd35-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-339">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-341">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7fd35-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7fd35-342">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-343">**Monitorhersteller**</span><span class="sxs-lookup"><span data-stu-id="7fd35-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-346">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="7fd35-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-347">Der Name des Monitor Herstellers.</span><span class="sxs-lookup"><span data-stu-id="7fd35-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="7fd35-348">Beispiel: "NEC"</span><span class="sxs-lookup"><span data-stu-id="7fd35-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-349">**Monitortyp**</span><span class="sxs-lookup"><span data-stu-id="7fd35-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-352">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="7fd35-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-353">Der Monitortyp.</span><span class="sxs-lookup"><span data-stu-id="7fd35-353">Type of monitor.</span></span>

<span data-ttu-id="7fd35-354">Beispiel: "NEC 5F GP"</span><span class="sxs-lookup"><span data-stu-id="7fd35-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-355">**Name**</span><span class="sxs-lookup"><span data-stu-id="7fd35-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-358">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7fd35-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-359">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-359">Label by which the object is known.</span></span> <span data-ttu-id="7fd35-360">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7fd35-361">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-362">**Pixelsperxlogicalzoll**</span><span class="sxs-lookup"><span data-stu-id="7fd35-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-363">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-365">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel pro logischem Zoll")</span><span class="sxs-lookup"><span data-stu-id="7fd35-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-366">Auflösung entlang der x-Achse (horizontale Richtung) des Monitors.</span><span class="sxs-lookup"><span data-stu-id="7fd35-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-367">**Pixelsperylogicalzoll**</span><span class="sxs-lookup"><span data-stu-id="7fd35-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-368">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-370">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel pro logischem Zoll")</span><span class="sxs-lookup"><span data-stu-id="7fd35-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-371">Auflösung entlang der y-Achse (vertikale Richtung) des Monitors.</span><span class="sxs-lookup"><span data-stu-id="7fd35-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7fd35-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-375">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7fd35-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-376">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7fd35-377">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7fd35-378">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7fd35-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-379">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="7fd35-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-380">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7fd35-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-382">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7fd35-383">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fd35-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7fd35-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7fd35-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7fd35-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-386">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7fd35-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="7fd35-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7fd35-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7fd35-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-389">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fd35-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7fd35-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="7fd35-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-391">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="7fd35-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7fd35-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="7fd35-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-393">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7fd35-394">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7fd35-395">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7fd35-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7fd35-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="7fd35-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-397">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7fd35-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="7fd35-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7fd35-399">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd35-400">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="7fd35-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-401">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7fd35-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-403">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="7fd35-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="7fd35-404">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="7fd35-405">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-406">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="7fd35-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-407">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-409">Logische Höhe der Anzeige in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="7fd35-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="7fd35-410">Diese Eigenschaft wird von [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-411">**Bildschirmbreite**</span><span class="sxs-lookup"><span data-stu-id="7fd35-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-412">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd35-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-414">Logische Breite der Anzeige in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="7fd35-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="7fd35-415">Diese Eigenschaft wird von [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-416">**Status**</span><span class="sxs-lookup"><span data-stu-id="7fd35-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-417">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-419">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7fd35-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-420">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-420">Current status of the object.</span></span> <span data-ttu-id="7fd35-421">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7fd35-422">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="7fd35-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7fd35-423">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="7fd35-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7fd35-424">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7fd35-425">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7fd35-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7fd35-426">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7fd35-427">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7fd35-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7fd35-428">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7fd35-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7fd35-429">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7fd35-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7fd35-430">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7fd35-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fd35-431">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7fd35-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7fd35-432">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7fd35-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7fd35-433">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7fd35-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7fd35-434">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7fd35-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7fd35-435">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7fd35-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7fd35-436">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7fd35-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7fd35-437">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7fd35-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7fd35-438">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7fd35-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7fd35-439">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7fd35-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd35-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7fd35-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-441">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fd35-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-443">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7fd35-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-444">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7fd35-444">State of the logical device.</span></span> <span data-ttu-id="7fd35-445">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7fd35-446">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7fd35-447">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7fd35-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fd35-448">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7fd35-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7fd35-449">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7fd35-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7fd35-450">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="7fd35-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7fd35-451">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="7fd35-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd35-452">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7fd35-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-453">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-455">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7fd35-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-456">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="7fd35-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="7fd35-457">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-458">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="7fd35-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd35-459">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd35-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd35-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd35-461">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7fd35-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7fd35-462">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7fd35-462">Name of the scoping system.</span></span>

<span data-ttu-id="7fd35-463">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd35-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fd35-464">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fd35-464">Remarks</span></span>

<span data-ttu-id="7fd35-465">Die **Win32 \_ Desktopmonitor** -Klasse wird von [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md)abgeleitet, der von der [**CIM- \_ Anzeige**](cim-display.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="7fd35-466">**CIM \_ Die Anzeige** wird von [**CIM \_ userdevice**](cim-userdevice.md)abgeleitet, das von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="7fd35-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7fd35-467">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fd35-467">Examples</span></span>

<span data-ttu-id="7fd35-468">Das Beispiel [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell in der TechNet Gallery verwendet **Win32 \_ Desktopmonitor** für die Interaktion mit dem Visio-Automatisierungs Modell, um eine Visio-Zeichnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd35-469">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fd35-469">Requirements</span></span>



| <span data-ttu-id="7fd35-470">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fd35-470">Requirement</span></span> | <span data-ttu-id="7fd35-471">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd35-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd35-472">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fd35-472">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd35-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fd35-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fd35-474">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fd35-474">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd35-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd35-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fd35-476">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fd35-476">Namespace</span></span><br/>                | <span data-ttu-id="7fd35-477">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7fd35-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7fd35-478">MOF</span><span class="sxs-lookup"><span data-stu-id="7fd35-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fd35-479"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7fd35-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fd35-480">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd35-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd35-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd35-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd35-482">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fd35-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd35-483">**CIM- \_ Desktop Monitor**</span><span class="sxs-lookup"><span data-stu-id="7fd35-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="7fd35-484">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd35-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7fd35-485">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="7fd35-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

