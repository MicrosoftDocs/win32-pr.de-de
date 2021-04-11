---
description: Stellt ein Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126272"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="b9fcc-103">Win32 \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9fcc-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="b9fcc-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ Computersystem** stellt ein Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="b9fcc-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9fcc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9fcc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a><span data-ttu-id="b9fcc-107">Member</span><span class="sxs-lookup"><span data-stu-id="b9fcc-107">Members</span></span>

<span data-ttu-id="b9fcc-108">Die **Win32- \_ Computersystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b9fcc-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="b9fcc-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="b9fcc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9fcc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9fcc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9fcc-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b9fcc-111">Methods</span></span>

<span data-ttu-id="b9fcc-112">Die **Win32- \_ Computersystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="b9fcc-113">Methode</span><span class="sxs-lookup"><span data-stu-id="b9fcc-113">Method</span></span>                                                                                          | <span data-ttu-id="b9fcc-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9fcc-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9fcc-115">**JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="b9fcc-116">Fügt einer Domäne oder Arbeitsgruppe ein Computersystem hinzu.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="b9fcc-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="b9fcc-118">Benennt einen lokalen Computer um.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="b9fcc-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="b9fcc-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-120">Not implemented.</span></span> <span data-ttu-id="b9fcc-121">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="b9fcc-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="b9fcc-122">**UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="b9fcc-123">Entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="b9fcc-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9fcc-124">Properties</span></span>

<span data-ttu-id="b9fcc-125">Die **Win32- \_ Computersystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9fcc-126">**Adminpasswordstatus**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| adminpasswordstatus")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-130">System Hardware-Sicherheitseinstellungen für den Status des Administrator Kennworts.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9fcc-131">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9fcc-132">**Aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="b9fcc-133">**Nicht implementiert** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-134">**Unbekannt** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-135">**AutomaticManagedPagefile**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-139">**True** gibt an, dass das System die Auslagerungs Datei verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-140">**Automatikresetbootoption**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-141">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-144">**True** gibt an, dass die Startoption für automatisches Zurücksetzen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-145">**Automatikresetcapability**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-149">**True** gibt an, dass die automatische zurück Setzung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-150">**Bootoptiononlimit**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-153">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| Capabilites \| Boot Option on Limit")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-154">Das Limit für die Startoption ist on.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-154">Boot option limit is ON.</span></span> <span data-ttu-id="b9fcc-155">Identifiziert die System Aktion, wenn der **resetLimit** -Wert erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b9fcc-156">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="b9fcc-157">**Betriebssystem** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="b9fcc-158">**System Dienstprogramme** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="b9fcc-159">**Nicht neu starten** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-160">**Bootoptiononwatchdog**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-163">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23- \| Funktionen- \| Start Option")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-164">Der Typ der Neustart Aktion nach dem Zeitpunkt, an dem der Watchdog-Timer abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b9fcc-165">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="b9fcc-166">**Betriebssystem** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="b9fcc-167">**System Dienstprogramme** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="b9fcc-168">**Nicht neu starten** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-169">**Bootrompeten unterstützt**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-172">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-173">**True** gibt an, ob eine Start-ROM unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-174">**Bootstatus**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-175">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-177">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 32 \| System Startinformationen \| Start Status")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-178">Status und zusätzliche Datenfelder, die den Startstatus identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="b9fcc-179">Dieser Wert stammt vom **Start Status** Mitglied der **System Start Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b9fcc-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-181">**BootupState**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-184">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CleanBoot")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-185">Das System wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-185">System is started.</span></span> <span data-ttu-id="b9fcc-186">Der ausfallsichere Start umgeht die Benutzer Startdateien, die auch "SafeBoot" genannt werden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="b9fcc-187">Die folgende Liste enthält die erforderlichen Werte:</span><span class="sxs-lookup"><span data-stu-id="b9fcc-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="b9fcc-188">"Normaler Start"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="b9fcc-189">"Ausfallsicherer Start"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="b9fcc-190">"Ausfallsicherheit beim Netzwerkstart"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="b9fcc-191">**Normaler Start** (normaler Start)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="b9fcc-192">**Ausfallsicherer Start** ("ausfallsicherer Start")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="b9fcc-193">**Ausfallsicherheit mit dem Netzwerkstart** ("Ausfallsicherheit beim Netzwerkstart")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-194">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-197">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-198">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b9fcc-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-200">**ChassisBootupState**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-201">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-203">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| bootup State")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-204">Startstatus des Chassis.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="b9fcc-205">Dieser Wert stammt aus dem **Status des Start Zustands** des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9fcc-206">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-207">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="b9fcc-208">**Safe** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b9fcc-209">**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b9fcc-210">**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="b9fcc-211">**Nicht wiederherstellbar** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-212">**Chassisskunverber**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-215">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 3 \| Chassis- \| SKU-Nummer")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-216">Die SKU-Nummer des Chassis oder Gehäuses als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="b9fcc-217">Dieser Wert stammt aus dem **SKU-Nummer** -Member des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b9fcc-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-219">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-222">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-223">Der Name der ersten konkreten Klasse in der Vererbungs Kette einer Instanz.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="b9fcc-224">Sie können diese Eigenschaft mit anderen Eigenschaften der-Klasse verwenden, um alle Instanzen der-Klasse und ihrer Unterklassen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="b9fcc-225">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-226">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-227">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-228">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-229">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-230">Die Zeitspanne, für die das einheitliche Computersystem von der koordinierten Weltzeit (UTC) versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-231">**DaylightInEffect**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-232">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-234">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-235">Wenn der Wert **true** ist, ist der sommermodus auf on.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-236">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-239">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-240">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-240">Description of the object.</span></span>

<span data-ttu-id="b9fcc-241">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-242">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-245">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| GetComputerNameEx \| ComputerNameDnsHostname")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-246">Der Name des lokalen Computers gemäß dem DNS (Domain Nameserver).</span><span class="sxs-lookup"><span data-stu-id="b9fcc-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-247">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-250">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**wksta \_ Info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ LANGroup")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-251">Der Name der Domäne, zu der ein Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="b9fcc-252">Wenn der Computer nicht Teil einer Domäne ist, wird der Name der Arbeitsgruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="b9fcc-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-254">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-256">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (DS) Structures \| [**DsRole \_ Primary \_ Domain \_ Info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DsRole \_ Machine \_ Role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| machinerole")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-257">Rolle eines Computers in einer zugewiesenen Domänen Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="b9fcc-258">Eine Domänen Arbeitsgruppe ist eine Sammlung von Computern im gleichen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="b9fcc-259">Beispielsweise kann eine **DomainRole** -Eigenschaft anzeigen, dass ein Computer Mitglied einer Arbeitsstation ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="b9fcc-260">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="b9fcc-261">**Eigenständige Arbeits** Station (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="b9fcc-262">**Mitglieds** Arbeitsstation (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="b9fcc-263">**Eigenständiger Server** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="b9fcc-264">**Mitglieds Server** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="b9fcc-265">**Domänen Controller sichern** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="b9fcc-266">**Primärer Domänen Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-267">**Enabledaylightsavingstime**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-268">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-269">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-270">Aktiviert die Sommerzeit (DST) auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="b9fcc-271">Der Wert **true** gibt an, dass sich die Systemzeit vor oder nach dem Start oder Ende des DST auf eine Stunde vor oder nach dem Ende ändert.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="b9fcc-272">Der Wert **false** gibt an, dass die Systemzeit nicht in eine Stunde vor oder hinter dem DST beginnt oder endet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="b9fcc-273">Der Wert **null** gibt an, dass der DST-Status in einem System unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-274">**FrontPanelResetStatus**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-275">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-277">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| FrontPanelResetStatus")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-278">In der folgenden Tabelle sind die Hardware Sicherheitseinstellungen für die Schaltfläche Zurücksetzen auf einem Computer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9fcc-279">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9fcc-280">**Aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="b9fcc-281">**Nicht implementiert** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-282">**Unbekannt** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-283">**Hypervisorpresent**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-284">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-286">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-287">**True** gibt an, dass ein Hypervisor vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="b9fcc-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-289">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-290">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-292">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-293">**True** gibt an, dass ein Infrarot-Port (IR) auf einem Computersystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-294">**Initizuadinfo**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-295">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-297">Daten, die für die Suche nach dem anfänglichen Lade Gerät oder Start Dienst erforderlich sind, um den Start des Betriebssystems anzufordern.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="b9fcc-298">Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="b9fcc-299">**Windows Server 2008 R2:** Diese Eigenschaft ist verfügbar, aber leer.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-301">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-303">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-304">Das Objekt ist installiert.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-304">Object is installed.</span></span> <span data-ttu-id="b9fcc-305">Ein Objekt benötigt keinen Wert, um anzugeben, dass es installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="b9fcc-306">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-307">**KeyboardPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-308">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-310">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| KeyboardPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-311">System Hardware-Sicherheitseinstellungen für den Status des Tastatur Kennworts.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9fcc-312">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9fcc-313">**Aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="b9fcc-314">**Nicht implementiert** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-315">**Unbekannt** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-316">**Lastloadinfo**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-319">Ein Array Eintrag der **initizuadinfo** -Eigenschaft, die die Daten zum Starten des geladenen Betriebssystems enthält.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="b9fcc-320">Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-321">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-324">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-325">Name eines Computerherstellers.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="b9fcc-326">Beispiel: Adventure Works</span><span class="sxs-lookup"><span data-stu-id="b9fcc-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-327">**Modell**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-330">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Product Name")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-331">Produktname, den ein Hersteller an einen Computer übergibt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="b9fcc-332">Diese Eigenschaft muss über einen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-333">**Name**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-336">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-337">Schlüssel einer [**CIM- \_ System**](cim-system.md) Instanz in einer Unternehmensumgebung.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="b9fcc-338">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-339">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-342">Der Name des Computer System **namens** , der automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="b9fcc-343">Das [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt und seine Ableitungen sind Objekte der obersten Ebene des Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="b9fcc-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="b9fcc-344">Sie stellen den Bereich für verschiedene Komponenten bereit.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-344">They provide the scope for several components.</span></span> <span data-ttu-id="b9fcc-345">Es sind eindeutige [**CIM- \_ System**](cim-system.md) Schlüssel erforderlich, Sie können jedoch eine Heuristik definieren, um den Namen des **CIM- \_ Computer Systems** zu erstellen, der denselben Namen generiert, und unabhängig vom Discovery-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="b9fcc-346">Dies verhindert Inventur-und Verwaltungsprobleme, wenn das gleiche Asset oder die gleiche Entität mehrmals erkannt wird, aber nicht in ein Objekt aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="b9fcc-347">Die Verwendung einer heuristischen Empfehlung wird empfohlen, ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="b9fcc-348">Die Heuristik wird in der Common Model-Spezifikation von CIM V2 beschrieben und geht davon aus, dass die dokumentierten Regeln zum bestimmen und Zuweisen eines Namens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="b9fcc-349">Die Liste **NameFormat** -Werte definiert die Reihenfolge, in der ein Computersystem Name zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="b9fcc-350">Mehrere Regeln werden demselben Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-350">Several rules map to the same value.</span></span>

<span data-ttu-id="b9fcc-351">Der Wert des [**CIM \_ Computersystem-namens**](cim-computersystem.md) , der mithilfe der Heuristik berechnet wird, ist der Schlüsselwert des Systems.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="b9fcc-352">Verwenden Sie jedoch Aliase, um einen anderen Namen für **CIM \_ Computersystem** zuzuweisen, der für Ihr Unternehmen eindeutiger ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="b9fcc-353">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="b9fcc-354">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="b9fcc-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="b9fcc-355">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="b9fcc-356">**Dial** ("Dial")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="b9fcc-357">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="b9fcc-358">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="b9fcc-359">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="b9fcc-360">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="b9fcc-361">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="b9fcc-362">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="b9fcc-363">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="b9fcc-364">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="b9fcc-365">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="b9fcc-366">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="b9fcc-367">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9fcc-368">**Sonstige** ("Sonstige")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-369">**Network Server modefähig**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-370">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-372">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Server \_ Info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| SV \_ Type \_ Server")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-373">**True** gibt an, dass der Netzwerk Server Modus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-374">**"Numoflogicalprocessor"**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-375">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-377">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-378">Anzahl der auf dem Computer verfügbaren logischen Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="b9fcc-379">Mithilfe von " **numoflogicalprocessor** " und " **numofprocessor** " können Sie ermitteln, ob der Computer Hyperthreading ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="b9fcc-380">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-382">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-384">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ Info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwnumofprocessor")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-385">Anzahl der physischen Prozessoren, die zurzeit auf einem System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="b9fcc-386">Dies ist die Anzahl der aktivierten Prozessoren für ein System, das die deaktivierten Prozessoren nicht einschließt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="b9fcc-387">Wenn ein Computersystem über zwei physische Prozessoren verfügt, die jeweils zwei logische Prozessoren enthalten, ist der Wert von " **numofprocessor** " 2, und " **numoflogicalprocessor** " ist 4.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="b9fcc-388">Dabei kann es sich um mehr Kern Prozessoren oder um Hyperthreading-Prozessoren handeln.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="b9fcc-389">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-390">**Oemlogobitmap**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-391">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-393">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-394">Liste der Daten für eine Bitmap, die der Originalgerätehersteller (OEM) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-395">**Oemstringarray**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-396">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-398">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 11 \| OEM Strings")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-399">Liste der frei Form Zeichenfolgen, die von einem OEM definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="b9fcc-400">Ein OEM definiert z. b. die Teilenummern für System Verweis Dokumente, Hersteller Kontaktinformationen usw.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-401">**"Element Domäne"**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-402">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-404">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-405">**True** gibt an, dass der Computer Teil einer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="b9fcc-406">Wenn der Wert **null** ist, befindet sich der Computer nicht in einer Domäne, oder der Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="b9fcc-407">Wenn Sie den Computer aus einer Domäne entfernen, wird der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-408">**Pausegafterreset**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-409">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-411">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 23 \| Timeout"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-412">Zeitverzögerung vor dem Initiieren eines Neustarts in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="b9fcc-413">Es wird nach einem System Energie-, System-oder Remote System-Reset und automatischer System Zurücksetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="b9fcc-414">Der Wert 1 (minus 1) gibt an, dass der Pausen Wert unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="b9fcc-415">**Windows Vista:** Diese Eigenschaft gibt möglicherweise eine unbekannte Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-416">**Pcsystemtype**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-417">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-419">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-420">Typ des verwendeten Computers, z. b. Laptop, Desktop oder Tablet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="b9fcc-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Nicht angegeben** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="b9fcc-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="b9fcc-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobil** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="b9fcc-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Arbeits** Station (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="b9fcc-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="b9fcc-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Soho-Server** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-427">Small Office-und Home Office-Server (Soho)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="b9fcc-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance-PC** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="b9fcc-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Leistungs Server** (7)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="b9fcc-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-431">**Pcsystemtypeex**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-432">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-434">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-435">Typ des verwendeten Computers, z. b. Laptop, Desktop oder Tablet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="b9fcc-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="b9fcc-437">**Nicht angegeben** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="b9fcc-438">**Desktop** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="b9fcc-439">**Mobil** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="b9fcc-440">**Arbeits** Station (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="b9fcc-441">**Enterprise Server** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="b9fcc-442">**Soho-Server** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="b9fcc-443">**Appliance-PC** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="b9fcc-444">**Leistungs Server** (7)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="b9fcc-445">**Slate** (8)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="b9fcc-446">**Maximum** (9)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-447">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-448">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-450">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Energiesteuerung \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-451">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b9fcc-452">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b9fcc-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9fcc-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9fcc-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-457">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b9fcc-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-459">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b9fcc-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-461">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b9fcc-462">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b9fcc-463">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b9fcc-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b9fcc-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-465">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b9fcc-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-467">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-467">Timed Power-On Supported</span></span>

<span data-ttu-id="b9fcc-468">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-469">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-470">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-471">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-472">**True** gibt an, dass das Gerät Energie gesteuert werden kann, z. b. Wenn ein Gerät in den Unterbrechungs Modus versetzt werden kann usw.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="b9fcc-473">Diese Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen derzeit aktiviert sind, gibt jedoch an, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="b9fcc-474">Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-475">**PowerOnPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-476">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-478">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| PowerOnPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-479">System Hardware-Sicherheitseinstellungen für Power-On Kenn Wort Status</span><span class="sxs-lookup"><span data-stu-id="b9fcc-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9fcc-480">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9fcc-481">**Aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="b9fcc-482">**Nicht implementiert** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-483">**Unbekannt** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-484">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-485">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-487">Aktueller Energiezustand eines Computers und des zugehörigen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="b9fcc-488">Die Energiespar Zustände weisen die folgenden Werte auf: Wert 4 (unbekannt) gibt an, dass sich das System bekanntermaßen in einem Energiesparmodus befindet, aber der genaue Status in diesem Modus ist unbekannt. 2 (niedriger Energie Modus) zeigt an, dass sich das System in einem Energiespar Zustand befindet, aber noch funktionsfähig ist und eine Beeinträchtigung der Leistung aufweisen kann. 3 (Standby) gibt an, dass das System nicht funktioniert, aber schnell in den vollständigen Energiesparmodus versetzt werden kann. und 7 (Warnung) gibt an, dass sich das Computersystem in einem Warnungs Status und in einem Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="b9fcc-489">Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="b9fcc-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Vollstrom** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b9fcc-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b9fcc-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b9fcc-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b9fcc-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b9fcc-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b9fcc-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (7)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="b9fcc-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Energiespar Speicher-** Ruhezustand (8)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-499">Energie sparen Sie den Ruhezustand.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="b9fcc-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save-Soft Off** (9)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-501">Power Save Soft aus.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-502">**PowerSupplyState**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-503">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-505">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 3- \| System Gehäuse oder Gehäuse \| Stromversorgung-Status")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-506">Der Status der Stromversorgung oder der Bereitstellung beim letzten starten.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="b9fcc-507">Dieser Wert stammt **aus dem** statusstatusmember des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b9fcc-508">In der folgenden Liste sind die Werte für diese Eigenschaft aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9fcc-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="b9fcc-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b9fcc-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b9fcc-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="b9fcc-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Nicht wiederherstellbar** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-515">Nicht BEHEB barer</span><span class="sxs-lookup"><span data-stu-id="b9fcc-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-516">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-517">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-518">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-519">Kontaktinformationen für den primären Systembesitzer, z. b. Telefonnummer, e-Mail-Adresse usw.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="b9fcc-520">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-521">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-522">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-523">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-524">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-525">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-525">Name of the primary system owner.</span></span>

<span data-ttu-id="b9fcc-526">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-527">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-528">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-529">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-530">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| System Hardware Security \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-531">Wenn diese Option aktiviert ist, ist der Wert 4, und das einheitliche Computersystem kann mithilfe der Schaltflächen Strom und Zurücksetzen zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="b9fcc-532">Wenn diese Option deaktiviert ist, ist der Wert 3, und eine zurück Setzung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="b9fcc-533">Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9fcc-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9fcc-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9fcc-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="b9fcc-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Nicht implementiert** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b9fcc-539">Nicht BEHEB barer</span><span class="sxs-lookup"><span data-stu-id="b9fcc-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-540">**ResetCount**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-541">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-543">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| Systemreset \| Reset count")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-544">Anzahl der automatischen zurück setzungen seit dem letzten Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="b9fcc-545">Der Wert 1 (minus 1) gibt an, dass die Anzahl unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-546">**ResetLimit**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-547">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-549">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 23 \| System Reset \| Reset Limit")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-550">Anzahl der aufeinander folgenden Versuche beim Zurücksetzen des Systems.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="b9fcc-551">Der Wert 1 (minus 1) gibt an, dass der Grenzwert unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-552">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-553">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-554">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-555">Liste, in der die Rollen eines Systems in der Informationstechnologie Umgebung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="b9fcc-556">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-557">**Status**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-558">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-559">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-560">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-561">Aktueller Status eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-561">Current status of an object.</span></span>

<span data-ttu-id="b9fcc-562">Für Win32_ComputerSystem lautet der Status immer "OK".</span><span class="sxs-lookup"><span data-stu-id="b9fcc-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="b9fcc-563">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="b9fcc-564">**Supportcontactdescription**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-565">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-566">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-567">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| Support Information")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-568">Liste der Kontaktinformationen des Supports für das Windows-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-569">**Systemfamilie**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-570">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-571">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-572">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Family")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-573">Die Familie, zu der ein bestimmter Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="b9fcc-574">Eine Familie bezieht sich auf eine Gruppe von Computern, die einer Hardware-oder Software Sicht ähnlich, aber nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="b9fcc-575">Dieser Wert stammt aus dem **Familien** Mitglied der **System Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b9fcc-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-577">**SystemSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-578">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-579">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-580">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| SKU Number")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-581">Identifiziert eine bestimmte Computerkonfiguration für den Verkauf.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="b9fcc-582">Manchmal auch als Produkt-ID oder Bestellnummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="b9fcc-583">Dieser Wert stammt aus dem **SKU-Nummern** Element der **System Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b9fcc-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-585">**SystemStartupDelay**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-586">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-587">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-588">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sesystemumgebungsprivileg"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**getprivateprofileint**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot Loader \| Timeout"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-589">**SystemStartupDelay** ist nicht mehr zur Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="b9fcc-590">Verwenden Sie stattdessen die vom WMI-Anbieter für Startkonfigurationsdaten (BCD) oder den Befehl **Bcdedit** bereitgestellten [BCD-Klassen](/previous-versions/windows/desktop/bcd/bcd-classes) .</span><span class="sxs-lookup"><span data-stu-id="b9fcc-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-591">**SystemStartupOptions**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-592">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b9fcc-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-593">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-594">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sesystemumgebungprivileg"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-595">**SystemStartupOptions** ist nicht mehr zur Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="b9fcc-596">Verwenden Sie stattdessen die vom WMI-Anbieter für Startkonfigurationsdaten (BCD) oder den Befehl **Bcdedit** bereitgestellten [BCD-Klassen](/previous-versions/windows/desktop/bcd/bcd-classes) .</span><span class="sxs-lookup"><span data-stu-id="b9fcc-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-597">**Systemstartupsetting**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-598">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-599">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-600">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sesystemumgebtungprivilege"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-601">**Systemstartupsetting** ist nicht mehr zur Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="b9fcc-602">Verwenden Sie stattdessen die vom WMI-Anbieter für Startkonfigurationsdaten (BCD) oder den Befehl **Bcdedit** bereitgestellten [BCD-Klassen](/previous-versions/windows/desktop/bcd/bcd-classes) .</span><span class="sxs-lookup"><span data-stu-id="b9fcc-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-603">**System Type**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-604">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-605">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-606">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ Info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wprocessorarchitecture")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-607">System, das auf dem Windows-basierten Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="b9fcc-608">Diese Eigenschaft muss über einen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-608">This property must have a value.</span></span>

<span data-ttu-id="b9fcc-609">In der folgenden Liste sind einige der möglichen Werte für diese Eigenschaft aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="b9fcc-610">"x64-basierter PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-611">"X86-basierter PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-612">"MIPS-basierter PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-613">"Alpha basierter PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-614">"Power PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-615">"Sh-x PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-616">"StrongARM-PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-617">"64-Bit-Intel-PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-618">"64-Bit-Alpha-PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="b9fcc-619">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="b9fcc-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="b9fcc-620">"X86-Nec98 PC"</span><span class="sxs-lookup"><span data-stu-id="b9fcc-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="b9fcc-621">**X86-basierter PC** (x86-basierter PC)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="b9fcc-622">**MIPS-basierter PC** ("MIPS-basierter PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="b9fcc-623">**Alpha basierter PC** ("Alpha basierter PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="b9fcc-624">**Power PC** ("Power PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="b9fcc-625">**SH-x PC** ("sh-x PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="b9fcc-626">**StrongARM-PC** ("StrongARM-PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="b9fcc-627">**64-Bit-Intel-PC** ("64-Bit Intel PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="b9fcc-628">**x64-basierter PC** ("x64-basierter PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-629">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="b9fcc-630">**X86-Nec98 PC** ("x86-Nec98 PC")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-631">**Thermalzustand**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-632">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-633">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-634">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 3- \| System Gehäuse oder Gehäuse- \| wärmezustand")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-635">Der thermische Zustand des Systems beim letzten starten.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="b9fcc-636">Dieser Wert stammt aus dem **wärmestatusmember** des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9fcc-637">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-638">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="b9fcc-639">**Safe** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b9fcc-640">**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b9fcc-641">**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="b9fcc-642">**Nicht wiederherstellbar** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-644">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-645">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-646">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-647">Gesamtgröße des physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-647">Total size of physical memory.</span></span> <span data-ttu-id="b9fcc-648">Beachten Sie, dass diese Eigenschaft unter bestimmten Umständen keinen exakten Wert für den physischen Arbeitsspeicher zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="b9fcc-649">Beispielsweise ist es nicht korrekt, wenn das BIOS einen Teil des physischen Speichers verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="b9fcc-650">Verwenden Sie für einen exakten Wert stattdessen die **Capacity** -Eigenschaft im [**Win32- \_ PhysicalMemory**](win32-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="b9fcc-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="b9fcc-651">Beispiel: 67108864</span><span class="sxs-lookup"><span data-stu-id="b9fcc-651">Example: 67108864</span></span>

<span data-ttu-id="b9fcc-652">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9fcc-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-653">**UserName**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-654">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-655">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-656">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Functions \| [**GetUsername**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-657">Der Name eines Benutzers, der zurzeit angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="b9fcc-658">Diese Eigenschaft muss über einen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-658">This property must have a value.</span></span> <span data-ttu-id="b9fcc-659">In einer Terminaldienste-Sitzung gibt **username** den Namen des Benutzers zurück, der bei der Konsole nicht angemeldet ist, nicht den Benutzer, der während der Terminaldienst Sitzung angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="b9fcc-660">Beispiel: JeffSmith</span><span class="sxs-lookup"><span data-stu-id="b9fcc-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="b9fcc-661">**Wakeuptype**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-662">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-663">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9fcc-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-664">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information Reaktivierungs \| Type")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-665">Das Ereignis bewirkt, dass das System aufschlägt.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="b9fcc-666">Dieser Wert stammt aus dem Reaktivierungs **-Typmember** der **System Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b9fcc-667">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9fcc-668">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9fcc-669">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="b9fcc-670">**APM-Timer** (3)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="b9fcc-671">**Modem Ring** (4)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="b9fcc-672">**LAN-Remote** (5)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="b9fcc-673">**Netzschalter** (6)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="b9fcc-674">**PCI-PME \#** 19.00</span><span class="sxs-lookup"><span data-stu-id="b9fcc-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="b9fcc-675">**Stromversorgung wieder hergestellt** (8)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9fcc-676">**Arbeitsgruppe**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9fcc-677">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-678">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9fcc-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9fcc-679">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="b9fcc-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="b9fcc-680">Der Name der Arbeitsgruppe für diesen Computer.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="b9fcc-681">Wenn der Wert der Eigenschaft " **Parser** " auf " **false**" festgelegt ist, wird der Name der Arbeitsgruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9fcc-682">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9fcc-682">Remarks</span></span>

<span data-ttu-id="b9fcc-683">Verwenden Sie die [**Win32 \_ computersystemprocessor**](win32-computersystemprocessor.md) Association-Klasse, um die Gesamtanzahl der Prozessor Instanzen zu ermitteln, die einem Computersystem Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="b9fcc-684">Eine **Win32- \_ Computersystem** Instanz, der mehrere physische Prozessoren zugeordnet sind, sind mehrere [**Win32- \_ Prozessor**](win32-processor.md) Instanzen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="b9fcc-685">Wenn der Wert von " **numoflogicalprocessor** " größer als der Wert von " **numofprocessor** " ist, handelt es sich bei dem Computersystem entweder um ein Multikernsystem oder um einen oder mehrere Prozessoren, die für Hyperthreading aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="b9fcc-686">Weitere Informationen finden Sie im Abschnitt **zu den Eigenschaften** und Hinweisen im Abschnitt **"Eigenschaften und** Hinweise" im Win32- **\_ Prozessor**.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="b9fcc-687">Die **Win32- \_ Computersystem** -Klasse wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9fcc-688">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9fcc-688">Examples</span></span>

<span data-ttu-id="b9fcc-689">Im folgenden Skript Center- [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) wird das **Win32- \_ Computersystem** verwendet, um Informationen aus einer Reihe von Computersystemen abzurufen und in einer GUI anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="b9fcc-690">Ein Beispielskript, das Betriebssystem-und Prozessor Daten von **Win32 \_ Computersystem**, [**Win32 \_ Processor**](win32-processor.md)und [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) abruft, finden Sie in den Beispielen zu [**Win32- \_ Prozessor**](win32-processor.md) Themen.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="b9fcc-691">Im folgenden VBScript-Beispiel wird beschrieben, wie der Domänen Name des lokalen Computers aus Instanzen von **Win32 \_ Computersystem** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="b9fcc-692">Im folgenden Perl-Beispiel wird beschrieben, wie der lokale Computername aus den Instanzen von **Win32 \_ Computersystem** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="b9fcc-693">Im folgenden Perl-Beispiel wird beschrieben, wie der DNS-Domänen Name des lokalen Computers aus Instanzen von **Win32 \_ Computersystem** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b9fcc-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="b9fcc-694">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9fcc-694">Requirements</span></span>



| <span data-ttu-id="b9fcc-695">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9fcc-695">Requirement</span></span> | <span data-ttu-id="b9fcc-696">Wert</span><span class="sxs-lookup"><span data-stu-id="b9fcc-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9fcc-697">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-697">Minimum supported client</span></span><br/> | <span data-ttu-id="b9fcc-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9fcc-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9fcc-699">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9fcc-699">Minimum supported server</span></span><br/> | <span data-ttu-id="b9fcc-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9fcc-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9fcc-701">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9fcc-701">Namespace</span></span><br/>                | <span data-ttu-id="b9fcc-702">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b9fcc-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9fcc-703">MOF</span><span class="sxs-lookup"><span data-stu-id="b9fcc-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9fcc-704"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b9fcc-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9fcc-705">DLL</span><span class="sxs-lookup"><span data-stu-id="b9fcc-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9fcc-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9fcc-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9fcc-707">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9fcc-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9fcc-708">**CIM \_ unitarycomputersystem**</span><span class="sxs-lookup"><span data-stu-id="b9fcc-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="b9fcc-709">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9fcc-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b9fcc-710">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="b9fcc-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b9fcc-711">WMI-Tasks: Computer Hardware</span><span class="sxs-lookup"><span data-stu-id="b9fcc-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="b9fcc-712">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="b9fcc-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

