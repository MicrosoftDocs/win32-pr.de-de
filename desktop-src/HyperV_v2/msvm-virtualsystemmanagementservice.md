---
description: Stellt den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750169"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1e761-103">MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1e761-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1e761-104">Stellt den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="1e761-105">**MSVM \_ Virtualsystemmanagementservice** wird verwendet, um die Definition, Änderung und Löschung von virtuellen Computern zu steuern.</span><span class="sxs-lookup"><span data-stu-id="1e761-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="1e761-106">Außerdem gibt es Methoden zum Ausführen von Vorgängen auf virtuellen Computern, z. b. zum Klonen, snapshoten und zum Importieren oder Exportieren virtueller Maschinen.</span><span class="sxs-lookup"><span data-stu-id="1e761-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="1e761-107">Verwenden Sie [**MSVM \_ Computersystem**](msvm-computersystem.md), um Informationen zu virtuellen Computern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e761-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="1e761-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e761-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e761-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e761-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="1e761-110">Member</span><span class="sxs-lookup"><span data-stu-id="1e761-110">Members</span></span>

<span data-ttu-id="1e761-111">Die **MSVM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1e761-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="1e761-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e761-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e761-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e761-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e761-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e761-114">Methods</span></span>

<span data-ttu-id="1e761-115">Die **MSVM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1e761-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="1e761-116">Methode</span><span class="sxs-lookup"><span data-stu-id="1e761-116">Method</span></span>                                                                                                                 | <span data-ttu-id="1e761-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e761-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e761-118">**Addbootsourcesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="1e761-119">Fügt einer virtuellen Systemkonfiguration Start Quellen hinzu, wenn diese auf eine virtuelle Systemkonfiguration vom Typ "State" angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e761-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="1e761-120">**Addfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="1e761-121">Fügt der Konfiguration einer Ethernet-Verbindung mit einem virtuellen Computer Ethernet-Funktionseinstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e761-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="1e761-122">**Addspbrechannelchap**</span><span class="sxs-lookup"><span data-stu-id="1e761-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="1e761-123">Fügt einem synthetischen Fibre Channel-Port auf einem virtuellen Computer dh-CHAP-Parameter hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e761-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="1e761-124">**Addguestservicesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="1e761-125">Fügt einer virtuellen Systemkonfiguration Gast Dienst Einstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e761-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="1e761-126">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1e761-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="1e761-127">**Addkvpitems**</span><span class="sxs-lookup"><span data-stu-id="1e761-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="1e761-128">Fügt einem virtuellen Computer Schlüssel-Wert-Paare hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e761-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="1e761-129">**Adresssourcesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="1e761-130">Fügt der Konfiguration einer virtuellen Maschine Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e761-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="1e761-131">**Addsystemcomponentsettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="1e761-132">Fügt der Konfiguration eines virtuellen Systems generische Einstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e761-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="1e761-133">**Defineplannedsystem**</span><span class="sxs-lookup"><span data-stu-id="1e761-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="1e761-134">Definiert ein geplantes virtuelles System.</span><span class="sxs-lookup"><span data-stu-id="1e761-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="1e761-135">Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="1e761-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1e761-136">**Definesystem**</span><span class="sxs-lookup"><span data-stu-id="1e761-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="1e761-137">Erstellt eine neue Definition für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="1e761-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="1e761-138">**Destroysystem**</span><span class="sxs-lookup"><span data-stu-id="1e761-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="1e761-139">Löscht die Definition einer vorhandenen virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="1e761-140">**Diagnosenetworkconnection**</span><span class="sxs-lookup"><span data-stu-id="1e761-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="1e761-141">Diagnostizieren der Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="1e761-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="1e761-142">**Exportsystemdefinition**</span><span class="sxs-lookup"><span data-stu-id="1e761-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="1e761-143">Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="1e761-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="1e761-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="1e761-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="1e761-145">Gibt eine formatierte Fehlermeldungs Zeichenfolge für das angegebene Array von eingebetteten [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="1e761-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="1e761-146">**Generatewwpn**</span><span class="sxs-lookup"><span data-stu-id="1e761-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="1e761-147">Generiert einen Satz von World Wide Port Names (WWPNs).</span><span class="sxs-lookup"><span data-stu-id="1e761-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="1e761-148">**Getcurrentwwpnfromgenerator**</span><span class="sxs-lookup"><span data-stu-id="1e761-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="1e761-149">Bietet die Möglichkeit, den aktuellen World Wide Port Name (WWPN) anzuzeigen, ohne dass der WWPN reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="1e761-150">**GetDefinitionFileSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="1e761-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="1e761-151">Gibt Informationen zur Zusammenfassung der virtuellen Computer für die angegebenen Definitions Dateien der virtuellen Maschine zurück.</span><span class="sxs-lookup"><span data-stu-id="1e761-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="1e761-152">**Getsizeofsystemfiles**</span><span class="sxs-lookup"><span data-stu-id="1e761-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="1e761-153">Ruft die Gesamtgröße der Systemdateien des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="1e761-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="1e761-154">**Getsummaryinformation**</span><span class="sxs-lookup"><span data-stu-id="1e761-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="1e761-155">Gibt Zusammenfassungs Informationen für virtuelle Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="1e761-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="1e761-156">**Getvirtualsystemthumbnailimage**</span><span class="sxs-lookup"><span data-stu-id="1e761-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="1e761-157">Ruft ein Miniaturbild eines vorhandenen virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="1e761-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="1e761-158">**Importsnapshotdefinitions**</span><span class="sxs-lookup"><span data-stu-id="1e761-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="1e761-159">Durchsucht den angegebenen Ordner nach allen Momentaufnahme Definitions Dateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1e761-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="1e761-160">**Importsystemdefinition**</span><span class="sxs-lookup"><span data-stu-id="1e761-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="1e761-161">Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="1e761-162">**Modifydiskmergesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="1e761-163">Ändert die Daten der Datenträger zusammenlaufseinstellung.</span><span class="sxs-lookup"><span data-stu-id="1e761-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="1e761-164">**Modifyfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="1e761-165">Ändert die aktuellen Featureeinstellungen einer Ethernet-Verbindung einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="1e761-166">**Modifyguestservicesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="1e761-167">Ändert die Einstellungen des Gast Diensts.</span><span class="sxs-lookup"><span data-stu-id="1e761-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="1e761-168">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1e761-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="1e761-169">**Modifykvpitems**</span><span class="sxs-lookup"><span data-stu-id="1e761-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="1e761-170">Ändert vorhandene Schlüssel-Wert-Paare auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1e761-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="1e761-171">**Modifyresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="1e761-172">Ändert die Einstellungen der virtuellen Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e761-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="1e761-173">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="1e761-174">Ändert die Einstellungsdaten des dienstanders.</span><span class="sxs-lookup"><span data-stu-id="1e761-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="1e761-175">**Modifysystemcomponentsettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="1e761-176">Ändert die generischen Systemkomponenten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1e761-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="1e761-177">**Modifysystemsettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="1e761-178">Ändert die Einstellungen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="1e761-179">**Realizeplannedsystem**</span><span class="sxs-lookup"><span data-stu-id="1e761-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="1e761-180">Überprüft die Konfiguration einer geplanten virtuellen Maschine und konvertiert sie in eine erkannte virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="1e761-181">**Removebootsourcesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="1e761-182">Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="1e761-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="1e761-183">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, werden möglicherweise als Nebeneffekt Ressourcen des aktiven virtuellen Systems entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e761-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="1e761-184">**Removefeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="1e761-185">Entfernt Funktionseinstellungen aus einer Ethernet-Verbindung eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1e761-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="1e761-186">**Removefbrechannelchap**</span><span class="sxs-lookup"><span data-stu-id="1e761-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="1e761-187">Entfernt die dh-CHAP-Parameter aus einem synthetischen Fibre Channel-Port auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1e761-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="1e761-188">**Removeguestservicesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="1e761-189">Entfernt Gast Dienst Einstellungen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="1e761-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="1e761-190">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1e761-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="1e761-191">**Removekvpitems**</span><span class="sxs-lookup"><span data-stu-id="1e761-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="1e761-192">Entfernt vorhandene Schlüssel-Wert-Paare aus einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="1e761-193">**Removeresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="1e761-194">Entfernt die Einstellungen der virtuellen Ressource aus der Konfiguration einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="1e761-195">**Removesystemcomponentsettings**</span><span class="sxs-lookup"><span data-stu-id="1e761-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="1e761-196">Entfernt generische Komponenten Einstellungen aus einer virtuellen Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e761-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="1e761-197">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1e761-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="1e761-198">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e761-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="1e761-199">**Setguestnetworkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="1e761-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="1e761-200">Konfiguriert die Netzwerkadapter innerhalb des Gast Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="1e761-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="1e761-201">**Setinitialmachineconfigurationdata**</span><span class="sxs-lookup"><span data-stu-id="1e761-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="1e761-202">Legt die anfänglichen Computer Konfigurationsdaten eines virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="1e761-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="1e761-203">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="1e761-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="1e761-204">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e761-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="1e761-205">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="1e761-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="1e761-206">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e761-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="1e761-207">**Testnetworkconnection**</span><span class="sxs-lookup"><span data-stu-id="1e761-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="1e761-208">Testet die Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="1e761-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="1e761-209">**Upgradesystemversion**</span><span class="sxs-lookup"><span data-stu-id="1e761-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="1e761-210">Führt ein Upgrade des virtuellen Systems durch.</span><span class="sxs-lookup"><span data-stu-id="1e761-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="1e761-211">Bei Anwendung auf die Systemeinstellungen einer "aktuellen" virtuellen Systemkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1e761-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="1e761-212">**Validateplannedsystem**</span><span class="sxs-lookup"><span data-stu-id="1e761-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="1e761-213">Überprüft das angegebene geplante System.</span><span class="sxs-lookup"><span data-stu-id="1e761-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="1e761-214">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e761-214">Properties</span></span>

<span data-ttu-id="1e761-215">Die **MSVM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e761-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e761-216">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="1e761-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-217">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1e761-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1e761-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-219">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="1e761-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1e761-220">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-221">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1e761-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-224">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e761-224">A short description of the object.</span></span> <span data-ttu-id="1e761-225">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Management Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-226">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="1e761-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-227">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-229">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1e761-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1e761-230">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1e761-231">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1e761-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1e761-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1e761-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="1e761-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="1e761-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="1e761-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1e761-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1e761-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1e761-239">)</span><span class="sxs-lookup"><span data-stu-id="1e761-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e761-240">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1e761-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-243">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1e761-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-244">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e761-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1e761-245">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ virtualsystemmanagementservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-246">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e761-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-249">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e761-249">A description of the object.</span></span> <span data-ttu-id="1e761-250">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Service zum Erstellen, bearbeiten und Verwalten virtueller Maschinen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1e761-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-252">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-254">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="1e761-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1e761-255">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1e761-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1e761-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="1e761-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="1e761-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="1e761-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="1e761-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="1e761-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="1e761-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1e761-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1e761-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1e761-265">)</span><span class="sxs-lookup"><span data-stu-id="1e761-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e761-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1e761-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-269">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1e761-269">A display name for the object.</span></span> <span data-ttu-id="1e761-270">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Management Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-271">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="1e761-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-272">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-274">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1e761-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1e761-275">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1e761-276">Wert</span><span class="sxs-lookup"><span data-stu-id="1e761-276">Value</span></span>                                                                        | <span data-ttu-id="1e761-277">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e761-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1e761-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1e761-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1e761-279">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="1e761-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1e761-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1e761-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-281">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-283">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1e761-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1e761-284">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="1e761-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="1e761-285">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1e761-286">Wert</span><span class="sxs-lookup"><span data-stu-id="1e761-286">Value</span></span>                                                                        | <span data-ttu-id="1e761-287">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e761-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1e761-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1e761-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1e761-289">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="1e761-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1e761-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1e761-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-291">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-293">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="1e761-293">The current health of the element.</span></span> <span data-ttu-id="1e761-294">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1e761-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1e761-295">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1e761-296">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="1e761-297">Wert</span><span class="sxs-lookup"><span data-stu-id="1e761-297">Value</span></span>                                                                        | <span data-ttu-id="1e761-298">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e761-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="1e761-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1e761-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="1e761-300">Der Integritäts Status ist "Normal".</span><span class="sxs-lookup"><span data-stu-id="1e761-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1e761-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1e761-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-302">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e761-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-304">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1e761-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1e761-305">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1e761-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e761-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-309">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1e761-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1e761-310">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1e761-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1e761-311">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1e761-312">**Name**</span><span class="sxs-lookup"><span data-stu-id="1e761-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-315">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1e761-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-316">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-316">The label by which the object is known.</span></span> <span data-ttu-id="1e761-317">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "VMMS" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-318">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="1e761-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-319">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-321">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1e761-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1e761-322">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1e761-323">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1e761-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1e761-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1e761-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="1e761-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="1e761-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="1e761-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="1e761-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="1e761-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="1e761-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="1e761-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="1e761-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="1e761-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="1e761-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="1e761-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="1e761-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="1e761-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="1e761-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="1e761-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1e761-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1e761-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1e761-343">)</span><span class="sxs-lookup"><span data-stu-id="1e761-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e761-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1e761-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-345">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1e761-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1e761-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-347">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e761-347">The current statuses of the object.</span></span> <span data-ttu-id="1e761-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1e761-349">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="1e761-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-352">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="1e761-353">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1e761-354">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-355">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1e761-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-358">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1e761-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-359">Alle Informationen dazu, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="1e761-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="1e761-360">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-361">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="1e761-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-362">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-364">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1e761-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-365">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="1e761-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="1e761-366">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="1e761-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="1e761-367">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-368">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="1e761-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-369">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-371">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="1e761-371">Provides high level status information.</span></span> <span data-ttu-id="1e761-372">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1e761-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1e761-373">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e761-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1e761-374">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1e761-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1e761-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1e761-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="1e761-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="1e761-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1e761-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1e761-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1e761-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1e761-381">)</span><span class="sxs-lookup"><span data-stu-id="1e761-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e761-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1e761-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-383">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-385">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="1e761-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="1e761-386">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1e761-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="1e761-387">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="1e761-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="1e761-388">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="1e761-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="1e761-389">Wenn dies auftritt, wird der Wert 12 ("nicht zutreffend") verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e761-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="1e761-390">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="1e761-391">Wert</span><span class="sxs-lookup"><span data-stu-id="1e761-391">Value</span></span>                                                                         | <span data-ttu-id="1e761-392">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e761-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="1e761-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1e761-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1e761-394">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1e761-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1e761-395">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="1e761-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-396">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1e761-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-398">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e761-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="1e761-399">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-400">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1e761-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-403">Qualifizierer: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="1e761-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-404">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1e761-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="1e761-405">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-406">**Status**</span><span class="sxs-lookup"><span data-stu-id="1e761-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-407">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-409">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e761-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1e761-410">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="1e761-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-411">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1e761-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1e761-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-413">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1e761-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1e761-414">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "der Dienst wird normal ausgeführt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-415">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="1e761-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-416">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-418">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1e761-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-419">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1e761-419">The scoping system's creation class name.</span></span> <span data-ttu-id="1e761-420">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="1e761-421">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="1e761-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-422">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e761-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e761-424">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1e761-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1e761-425">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="1e761-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="1e761-426">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1e761-427">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="1e761-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-428">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e761-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-430">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e761-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1e761-431">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e761-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1e761-432">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="1e761-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e761-433">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e761-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e761-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e761-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e761-435">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="1e761-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1e761-436">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e761-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e761-437">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e761-437">Remarks</span></span>

<span data-ttu-id="1e761-438">Der Zugriff auf die **MSVM \_ virtualsystemmanagementservice** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1e761-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1e761-439">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1e761-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e761-440">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e761-440">Requirements</span></span>



| <span data-ttu-id="1e761-441">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e761-441">Requirement</span></span> | <span data-ttu-id="1e761-442">Wert</span><span class="sxs-lookup"><span data-stu-id="1e761-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e761-443">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e761-443">Minimum supported client</span></span><br/> | <span data-ttu-id="1e761-444">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e761-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1e761-445">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e761-445">Minimum supported server</span></span><br/> | <span data-ttu-id="1e761-446">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e761-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e761-447">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e761-447">Namespace</span></span><br/>                | <span data-ttu-id="1e761-448">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1e761-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1e761-449">MOF</span><span class="sxs-lookup"><span data-stu-id="1e761-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e761-450"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1e761-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e761-451">DLL</span><span class="sxs-lookup"><span data-stu-id="1e761-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e761-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e761-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e761-453">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e761-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e761-454">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="1e761-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="1e761-455">[**CIM \_ virtualsystemmanagementservice**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e761-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1e761-456">[**MSVM \_ virtualsystemmanagementservice (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e761-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1e761-457">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="1e761-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

