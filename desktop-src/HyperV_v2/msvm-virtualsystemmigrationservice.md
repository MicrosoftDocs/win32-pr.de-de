---
description: Stellt den Dienst für die virtuelle System Migration dar. Sie wird zum Migrieren eines virtuellen Systems oder zum Migrieren des Speichers eines virtuellen Systems von einer Virtualisierungsplattform zu einem anderen verwendet.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750153"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="b1bba-104">MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b1bba-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="b1bba-105">Stellt den Dienst für die virtuelle System Migration dar.</span><span class="sxs-lookup"><span data-stu-id="b1bba-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="b1bba-106">Sie wird zum Migrieren eines virtuellen Systems oder zum Migrieren des Speichers eines virtuellen Systems von einer Virtualisierungsplattform zu einem anderen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1bba-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="b1bba-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1bba-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1bba-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="b1bba-109">Member</span><span class="sxs-lookup"><span data-stu-id="b1bba-109">Members</span></span>

<span data-ttu-id="b1bba-110">Die **MSVM \_ virtualsystemmigrationservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1bba-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="b1bba-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b1bba-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1bba-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1bba-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1bba-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b1bba-113">Methods</span></span>

<span data-ttu-id="b1bba-114">Die **MSVM \_ virtualsystemmigrationservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b1bba-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="b1bba-115">Methode</span><span class="sxs-lookup"><span data-stu-id="b1bba-115">Method</span></span>                                                                                                                  | <span data-ttu-id="b1bba-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1bba-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1bba-117">**Addnetworksettings**</span><span class="sxs-lookup"><span data-stu-id="b1bba-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="b1bba-118">Fügt Subnetze für die Migration des virtuellen System Migrations Dienstanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="b1bba-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="b1bba-119">**Checksystemcompatibilityinfo**</span><span class="sxs-lookup"><span data-stu-id="b1bba-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="b1bba-120">Überprüft die Kompatibilitätsinformationen auf die Kompatibilität mit dem hostingcomputersystem.</span><span class="sxs-lookup"><span data-stu-id="b1bba-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="b1bba-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="b1bba-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="b1bba-122">Methode zum Migrieren eines virtuellen Systems oder des Speichers eines virtuellen Systems zu einem durch einen Hostnamen angegebenen Zielhost.</span><span class="sxs-lookup"><span data-stu-id="b1bba-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="b1bba-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="b1bba-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="b1bba-124">Bestimmt, ob das angegebene virtuelle System zu einem Zielhost migriert werden kann, der von einem Netzwerknamen oder einer IP-Adresse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1bba-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="b1bba-125">**Getsystemcompatibilityinfo**</span><span class="sxs-lookup"><span data-stu-id="b1bba-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="b1bba-126">Generiert ein undurchsichtiges BLOB von Daten, das Kompatibilitätsinformationen für das angegebene System enthält.</span><span class="sxs-lookup"><span data-stu-id="b1bba-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="b1bba-127">**Getsystemcompatibilityvectors**</span><span class="sxs-lookup"><span data-stu-id="b1bba-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="b1bba-128">Ruft Kompatibilitäts Vektoren für eine virtuelle Maschine oder einen Host ab.</span><span class="sxs-lookup"><span data-stu-id="b1bba-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="b1bba-129">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="b1bba-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="b1bba-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="b1bba-131">Migriert ein virtuelles System oder den Speicher eines virtuellen Systems zu einem Zielhost, der durch einen Hostnamen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1bba-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="b1bba-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="b1bba-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="b1bba-133">Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.</span><span class="sxs-lookup"><span data-stu-id="b1bba-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="b1bba-134">**Modifynetworksettings**</span><span class="sxs-lookup"><span data-stu-id="b1bba-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="b1bba-135">Ändert die Migrations Netzwerksubnetze des virtuellen System Migrations Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b1bba-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="b1bba-136">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="b1bba-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="b1bba-137">Ändert die Einstellungsdaten für den Migrationsdienst.</span><span class="sxs-lookup"><span data-stu-id="b1bba-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="b1bba-138">**Removenetworksettings**</span><span class="sxs-lookup"><span data-stu-id="b1bba-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="b1bba-139">Entfernt die Subnetze des Migrationsnetzwerks aus dem virtuellen System Migrationsdienst.</span><span class="sxs-lookup"><span data-stu-id="b1bba-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="b1bba-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b1bba-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="b1bba-141">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="b1bba-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="b1bba-142">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="b1bba-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="b1bba-143">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="b1bba-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="b1bba-144">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="b1bba-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="b1bba-145">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="b1bba-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="b1bba-146">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1bba-146">Properties</span></span>

<span data-ttu-id="b1bba-147">Die **MSVM \_ virtualsystemmigrationservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1bba-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1bba-148">**Activestoragemigrationcount**</span><span class="sxs-lookup"><span data-stu-id="b1bba-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1bba-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-151">Die Anzahl der aktuellen Speicher Migrationen, die gerade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b1bba-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-152">**Activevirtualsystemmigrationcount**</span><span class="sxs-lookup"><span data-stu-id="b1bba-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1bba-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-155">Die Anzahl der aktuellen virtuellen System Migrationen, die gerade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b1bba-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-156">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="b1bba-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-157">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b1bba-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-159">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="b1bba-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="b1bba-160">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b1bba-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-164">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1bba-164">A short description of the object.</span></span> <span data-ttu-id="b1bba-165">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Migrationsdienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-166">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="b1bba-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-169">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="b1bba-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b1bba-170">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b1bba-171">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-172">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b1bba-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-175">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1bba-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b1bba-176">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ virtualsystemmigrationservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-177">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1bba-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-180">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1bba-180">A description of the object.</span></span> <span data-ttu-id="b1bba-181">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Migrationsdienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b1bba-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-185">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="b1bba-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b1bba-186">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b1bba-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b1bba-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-191">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-191">A display name for the object.</span></span> <span data-ttu-id="b1bba-192">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Migrationsdienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-193">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="b1bba-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-194">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-196">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b1bba-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b1bba-197">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b1bba-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-201">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b1bba-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b1bba-202">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="b1bba-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="b1bba-203">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b1bba-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-205">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-207">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="b1bba-207">The current health of the element.</span></span> <span data-ttu-id="b1bba-208">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="b1bba-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b1bba-209">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b1bba-210">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1bba-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-212">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1bba-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-214">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="b1bba-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="b1bba-215">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1bba-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-219">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b1bba-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-220">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b1bba-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b1bba-221">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-222">**Migrationservicelisteneripaddresslist**</span><span class="sxs-lookup"><span data-stu-id="b1bba-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-223">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b1bba-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-225">Die Liste der Host-IP-Adressen, die für die Migration des virtuellen Systems verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b1bba-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-226">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1bba-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-229">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-229">The label by which the object is known.</span></span> <span data-ttu-id="b1bba-230">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "migrationwmi" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-231">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="b1bba-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-232">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-234">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b1bba-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b1bba-235">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b1bba-236">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b1bba-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-238">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b1bba-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-240">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1bba-240">The current statuses of the object.</span></span> <span data-ttu-id="b1bba-241">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-242">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="b1bba-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-245">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b1bba-246">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b1bba-247">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="b1bba-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-251">Ein Wert, der Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="b1bba-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="b1bba-252">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-253">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="b1bba-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-256">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="b1bba-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="b1bba-257">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="b1bba-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="b1bba-258">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-259">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="b1bba-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-260">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-262">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="b1bba-262">Provides high level status information.</span></span> <span data-ttu-id="b1bba-263">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b1bba-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b1bba-264">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1bba-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b1bba-265">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b1bba-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-269">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="b1bba-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="b1bba-270">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="b1bba-271">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="b1bba-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="b1bba-272">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="b1bba-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="b1bba-273">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1bba-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="b1bba-274">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-275">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="b1bba-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-276">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b1bba-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-278">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1bba-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="b1bba-279">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="b1bba-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-283">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b1bba-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="b1bba-284">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-285">**Status**</span><span class="sxs-lookup"><span data-stu-id="b1bba-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-289">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="b1bba-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-290">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b1bba-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-292">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b1bba-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b1bba-293">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und die Zeichen folgen sind immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-294">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b1bba-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-297">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="b1bba-297">The scoping system's creation class name.</span></span> <span data-ttu-id="b1bba-298">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-299">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="b1bba-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1bba-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-302">Der Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="b1bba-302">The name of the hosting computer system.</span></span> <span data-ttu-id="b1bba-303">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-304">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="b1bba-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-305">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1bba-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-307">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b1bba-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b1bba-308">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b1bba-309">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="b1bba-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bba-310">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1bba-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bba-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1bba-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1bba-312">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="b1bba-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b1bba-313">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1bba-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1bba-314">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1bba-314">Requirements</span></span>



| <span data-ttu-id="b1bba-315">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1bba-315">Requirement</span></span> | <span data-ttu-id="b1bba-316">Wert</span><span class="sxs-lookup"><span data-stu-id="b1bba-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bba-317">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1bba-317">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bba-318">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1bba-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b1bba-319">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1bba-319">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bba-320">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1bba-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1bba-321">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1bba-321">Namespace</span></span><br/>                | <span data-ttu-id="b1bba-322">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b1bba-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b1bba-323">MOF</span><span class="sxs-lookup"><span data-stu-id="b1bba-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1bba-324"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b1bba-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1bba-325">DLL</span><span class="sxs-lookup"><span data-stu-id="b1bba-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1bba-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1bba-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

