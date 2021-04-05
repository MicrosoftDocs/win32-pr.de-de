---
description: Verwaltet die virtuellen Medien (VHD-, vhdx-, ISO-oder VFD-Dateien) für eine virtuelle Maschine.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752369"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="9c724-103">MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="9c724-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9c724-104">Verwaltet die virtuellen Medien (VHD-, vhdx-, ISO-oder VFD-Dateien) für eine virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="9c724-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="9c724-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c724-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c724-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c724-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="9c724-107">Member</span><span class="sxs-lookup"><span data-stu-id="9c724-107">Members</span></span>

<span data-ttu-id="9c724-108">Die **MSVM \_ imagemanagementservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9c724-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="9c724-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="9c724-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c724-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c724-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c724-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9c724-111">Methods</span></span>

<span data-ttu-id="9c724-112">Die **MSVM \_ imagemanagementservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9c724-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="9c724-113">Methode</span><span class="sxs-lookup"><span data-stu-id="9c724-113">Method</span></span>                                                                                                           | <span data-ttu-id="9c724-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c724-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c724-115">**Attachvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="9c724-116">Fügt eine virtuelle Festplatten Abbild Datei im Loopback Modus an.</span><span class="sxs-lookup"><span data-stu-id="9c724-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="9c724-117">**Compactvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="9c724-118">Komprimiert eine virtuelle Festplatten Datei.</span><span class="sxs-lookup"><span data-stu-id="9c724-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="9c724-119">**Convertvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="9c724-120">Konvertiert eine vorhandene virtuelle Festplatte in einen anderen Typ oder ein anderes Format.</span><span class="sxs-lookup"><span data-stu-id="9c724-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="9c724-121">**Convertvirtualharddisktovhdset**</span><span class="sxs-lookup"><span data-stu-id="9c724-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="9c724-122">Konvertiert eine virtuelle Festplatten Datei, indem eine neue VHD-Datei mit der vorhandenen virtuellen Festplatte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c724-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="9c724-123">**"Kreatevirtualfloppydisk"**</span><span class="sxs-lookup"><span data-stu-id="9c724-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="9c724-124">Erstellt eine virtuelle Disketten Datei.</span><span class="sxs-lookup"><span data-stu-id="9c724-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="9c724-125">**"Kreatevirtualharddisk"**</span><span class="sxs-lookup"><span data-stu-id="9c724-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="9c724-126">Erstellt eine virtuelle Festplatten Datei.</span><span class="sxs-lookup"><span data-stu-id="9c724-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="9c724-127">**Deletevhdsnapshot**</span><span class="sxs-lookup"><span data-stu-id="9c724-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="9c724-128">Löscht einen Eintrag für eine VHD-Momentaufnahme in einer VHD-Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="9c724-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="9c724-129">**Findmountedstorageimageinstance**</span><span class="sxs-lookup"><span data-stu-id="9c724-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="9c724-130">Sucht ein MSVM \_ mountedstorageimage-Objekt für einen angegebenen Datenträger-Bildpfad.</span><span class="sxs-lookup"><span data-stu-id="9c724-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="9c724-131">**Getvhdsetinformation**</span><span class="sxs-lookup"><span data-stu-id="9c724-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="9c724-132">Ruft Informationen zu einer VHD-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="9c724-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="9c724-133">**Getvhdsnapshotinformation**</span><span class="sxs-lookup"><span data-stu-id="9c724-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="9c724-134">Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="9c724-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="9c724-135">**Getvirtualdiskchanges**</span><span class="sxs-lookup"><span data-stu-id="9c724-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="9c724-136">Ruft eine Liste der Änderungen im angegebenen Bereich eines virtuellen Datenträgers ab, die von der angegebenen robusten Änderungsnachverfolgung ID oder der vhdset-Momentaufnahme-ID bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c724-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9c724-137">**Getvirtualharddisksettingdata**</span><span class="sxs-lookup"><span data-stu-id="9c724-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="9c724-138">Ruft Einstellungsdaten ab, die virtuellen Festplatten Dateien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9c724-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="9c724-139">**Getvirtualharddiskstate**</span><span class="sxs-lookup"><span data-stu-id="9c724-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="9c724-140">Ruft den Zustand der virtuellen Festplatten Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="9c724-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="9c724-141">**Mergevirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="9c724-142">Führt eine untergeordnete virtuelle Festplatte in einer differenzierenden Kette mit einer oder mehreren übergeordneten virtuellen Festplatten in der Kette zusammen.</span><span class="sxs-lookup"><span data-stu-id="9c724-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="9c724-143">**Optimizevhdset**</span><span class="sxs-lookup"><span data-stu-id="9c724-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="9c724-144">Optimiert eine VHD-Datei Satz Datei, um weniger Speicherplatz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c724-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="9c724-145">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9c724-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="9c724-146">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="9c724-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="9c724-147">**Resizevirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="9c724-148">Ändert die Größe einer vorhandenen virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="9c724-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="9c724-149">**SetParser-virtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="9c724-150">Aktualisiert das übergeordnete Element für das angegebene Blatt und die untergeordneten virtuellen Festplatten Dateien.</span><span class="sxs-lookup"><span data-stu-id="9c724-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="9c724-151">**Setvhdsnapshotinformation**</span><span class="sxs-lookup"><span data-stu-id="9c724-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="9c724-152">Bearbeitet einen VHD-momentaufnahmeneintrag innerhalb einer VHD-Datei.</span><span class="sxs-lookup"><span data-stu-id="9c724-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="9c724-153">Wenn die fragliche Momentaufnahme-ID bereits vorhanden ist, wird der vorhandene Momentaufnahme Eintrag mit dem neuen Eintrag überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9c724-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="9c724-154">Andernfalls wird der neue Eintrag der VHD-Satz Datei hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9c724-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="9c724-155">**Setvirtualharddisksettingdata**</span><span class="sxs-lookup"><span data-stu-id="9c724-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="9c724-156">Legt eine virtuelle Festplatten Datei fest.</span><span class="sxs-lookup"><span data-stu-id="9c724-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="9c724-157">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="9c724-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="9c724-158">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="9c724-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="9c724-159">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="9c724-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="9c724-160">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="9c724-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="9c724-161">**Validatepersistentreservationsupport**</span><span class="sxs-lookup"><span data-stu-id="9c724-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="9c724-162">Überprüft, ob ein Dateisystem eine virtuelle Festplatte mit aktivierten permanenten Reservierungen unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="9c724-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="9c724-163">**Validatevirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="9c724-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="9c724-164">Überprüft, ob ein virtuelles Festplatten Image im schreibgeschützten Modus geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c724-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="9c724-165">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c724-165">Properties</span></span>

<span data-ttu-id="9c724-166">Die **MSVM \_ imagemanagementservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c724-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c724-167">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="9c724-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-168">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9c724-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c724-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-170">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="9c724-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9c724-171">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9c724-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-175">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9c724-175">A short description of the object.</span></span> <span data-ttu-id="9c724-176">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Abbild Verwaltungsdienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="9c724-177">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="9c724-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-180">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="9c724-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9c724-181">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c724-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c724-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9c724-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="9c724-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9c724-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="9c724-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="9c724-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9c724-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9c724-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c724-190">)</span><span class="sxs-lookup"><span data-stu-id="9c724-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c724-191">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9c724-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-194">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c724-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9c724-195">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ imagemanagementservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="9c724-196">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c724-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-199">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9c724-199">A description of the object.</span></span> <span data-ttu-id="9c724-200">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Bereitstellen der Abbild Verwaltungs Wartung für Hyper-V" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="9c724-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9c724-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-204">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="9c724-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9c724-205">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c724-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c724-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="9c724-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="9c724-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="9c724-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="9c724-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="9c724-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="9c724-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9c724-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9c724-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c724-215">)</span><span class="sxs-lookup"><span data-stu-id="9c724-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c724-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9c724-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-219">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c724-219">A display name for the object.</span></span> <span data-ttu-id="9c724-220">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Abbild Verwaltungsdienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="9c724-221">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="9c724-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-222">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-224">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="9c724-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9c724-225">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9c724-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-227">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-229">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="9c724-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9c724-230">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="9c724-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9c724-231">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9c724-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-233">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-235">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="9c724-235">The current health of the element.</span></span> <span data-ttu-id="9c724-236">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9c724-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9c724-237">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9c724-238">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9c724-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-240">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c724-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-242">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="9c724-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9c724-243">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9c724-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c724-247">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9c724-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9c724-248">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9c724-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9c724-249">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-250">**Name**</span><span class="sxs-lookup"><span data-stu-id="9c724-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c724-253">Qualifizierer: **Key**, **override** ("Name"), **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="9c724-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9c724-254">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-254">The label by which the object is known.</span></span> <span data-ttu-id="9c724-255">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "vhdsvc" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="9c724-256">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="9c724-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-259">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9c724-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9c724-260">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c724-261">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c724-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9c724-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="9c724-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="9c724-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="9c724-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="9c724-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="9c724-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="9c724-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="9c724-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="9c724-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="9c724-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="9c724-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="9c724-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="9c724-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="9c724-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="9c724-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="9c724-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="9c724-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9c724-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9c724-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c724-281">)</span><span class="sxs-lookup"><span data-stu-id="9c724-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c724-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9c724-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-283">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9c724-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c724-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-285">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9c724-285">The current status of the object.</span></span> <span data-ttu-id="9c724-286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-287">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="9c724-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-290">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9c724-291">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9c724-292">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="9c724-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-296">Eine Zeichenfolge, die Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="9c724-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="9c724-297">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-298">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="9c724-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-301">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="9c724-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="9c724-302">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="9c724-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="9c724-303">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-304">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="9c724-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-305">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-307">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="9c724-307">Provides high level status information.</span></span> <span data-ttu-id="9c724-308">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9c724-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9c724-309">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9c724-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c724-310">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c724-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9c724-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9c724-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="9c724-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="9c724-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9c724-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c724-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9c724-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c724-317">)</span><span class="sxs-lookup"><span data-stu-id="9c724-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c724-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9c724-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-319">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-321">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="9c724-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="9c724-322">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9c724-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9c724-323">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="9c724-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9c724-324">**Requestedstatechange** wird von einer bestimmten Instanz von **enabledlogicalelement** möglicherweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c724-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="9c724-325">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c724-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="9c724-326">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-327">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="9c724-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-328">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9c724-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-330">Gibt an, ob der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9c724-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="9c724-331">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-332">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="9c724-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-335">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9c724-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="9c724-336">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-337">**Status**</span><span class="sxs-lookup"><span data-stu-id="9c724-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c724-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c724-341">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="9c724-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-342">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9c724-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c724-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-344">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9c724-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9c724-345">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-346">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="9c724-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-349">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="9c724-349">The scoping system's creation class name.</span></span> <span data-ttu-id="9c724-350">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="9c724-351">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="9c724-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c724-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-354">Der Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="9c724-354">The name of the hosting computer system.</span></span> <span data-ttu-id="9c724-355">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-356">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="9c724-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-357">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c724-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-359">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9c724-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9c724-360">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c724-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c724-361">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="9c724-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c724-362">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c724-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c724-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c724-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c724-364">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="9c724-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9c724-365">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c724-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c724-366">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c724-366">Remarks</span></span>

<span data-ttu-id="9c724-367">Der Zugriff auf die **MSVM \_ imagemanagementservice** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="9c724-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9c724-368">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9c724-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c724-369">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c724-369">Requirements</span></span>



| <span data-ttu-id="9c724-370">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c724-370">Requirement</span></span> | <span data-ttu-id="9c724-371">Wert</span><span class="sxs-lookup"><span data-stu-id="9c724-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c724-372">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c724-372">Minimum supported client</span></span><br/> | <span data-ttu-id="9c724-373">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c724-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c724-374">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c724-374">Minimum supported server</span></span><br/> | <span data-ttu-id="9c724-375">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c724-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c724-376">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c724-376">Namespace</span></span><br/>                | <span data-ttu-id="9c724-377">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9c724-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c724-378">MOF</span><span class="sxs-lookup"><span data-stu-id="9c724-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c724-379"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9c724-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c724-380">DLL</span><span class="sxs-lookup"><span data-stu-id="9c724-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c724-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c724-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c724-382">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c724-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c724-383">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="9c724-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="9c724-384">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="9c724-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="9c724-385">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="9c724-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

