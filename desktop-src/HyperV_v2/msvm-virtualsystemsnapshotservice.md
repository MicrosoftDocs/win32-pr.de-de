---
description: Dienst zum Erstellen, anwenden und zerstören von Momentaufnahmen von virtuellen Computern.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862051"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="2bb2e-103">MSVM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2bb2e-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="2bb2e-104">Dienst zum Erstellen, anwenden und zerstören von Momentaufnahmen von virtuellen Computern.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="2bb2e-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb2e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bb2e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="2bb2e-107">Member</span><span class="sxs-lookup"><span data-stu-id="2bb2e-107">Members</span></span>

<span data-ttu-id="2bb2e-108">Die **MSVM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2bb2e-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="2bb2e-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="2bb2e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2bb2e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bb2e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2bb2e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="2bb2e-111">Methods</span></span>

<span data-ttu-id="2bb2e-112">Die **MSVM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2bb2e-113">Methode</span><span class="sxs-lookup"><span data-stu-id="2bb2e-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2bb2e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bb2e-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2bb2e-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>Applysnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-116">Wendet eine Momentaufnahme des virtuellen Computers auf den virtuellen Computer an, auf dem Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2bb2e-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>Clearsnapshotstate</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-118">Löscht den Zustand speichern aus einer vorhandenen Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2bb2e-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>Converttoreferencepoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-120">Konvertieren einer vorhandenen Momentaufnahme eines virtuellen Systems in einen Referenzpunkt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="2bb2e-121">Die Momentaufnahme wird als Nebeneffekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="2bb2e-122">Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bb2e-123">Unterstützung für diese Methode wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2bb2e-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-125">Erstellt eine Momentaufnahme einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2bb2e-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>Destroysnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-127">Zerstört eine vorhandene Momentaufnahme des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="2bb2e-128">Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2bb2e-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>Destroysnapshottree</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-130">Entfernt eine vorhandene Momentaufnahme und alle untergeordneten Elemente eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2bb2e-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bb2e-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-132">Fordert eine Statusänderung für das Element an.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bb2e-133">Unterstützung für diese Methode wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2bb2e-134"><strong>Start Service</strong></span><span class="sxs-lookup"><span data-stu-id="2bb2e-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-135">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2bb2e-136"><strong>Stop Service</strong></span><span class="sxs-lookup"><span data-stu-id="2bb2e-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2bb2e-137">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="2bb2e-138">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bb2e-138">Properties</span></span>

<span data-ttu-id="2bb2e-139">Die **MSVM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bb2e-140">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-141">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2bb2e-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-143">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="2bb2e-144">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="2bb2e-145">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2bb2e-146">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2bb2e-147">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2bb2e-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="2bb2e-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="2bb2e-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="2bb2e-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="2bb2e-158">)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb2e-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-162">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-162">A short description of the object.</span></span> <span data-ttu-id="2bb2e-163">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Snapshot Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-164">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-167">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2bb2e-168">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2bb2e-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2bb2e-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="2bb2e-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2bb2e-177">)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb2e-178">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-181">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-182">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2bb2e-183">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ virtualsystemsnapshotservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-184">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-187">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-187">A description of the object.</span></span> <span data-ttu-id="2bb2e-188">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Service zum Erstellen, zerstören und Anwenden von Momentaufnahmen virtueller Computer" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-192">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2bb2e-193">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2bb2e-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2bb2e-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="2bb2e-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2bb2e-203">)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb2e-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-207">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-207">A display name for the object.</span></span> <span data-ttu-id="2bb2e-208">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-209">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-210">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-212">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2bb2e-213">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="2bb2e-214">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-214">Value</span></span>                                                                        | <span data-ttu-id="2bb2e-215">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2bb2e-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="2bb2e-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2bb2e-217">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2bb2e-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-219">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-221">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2bb2e-222">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="2bb2e-223">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="2bb2e-224">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-224">Value</span></span>                                                                        | <span data-ttu-id="2bb2e-225">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2bb2e-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="2bb2e-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2bb2e-227">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2bb2e-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-229">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-231">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-231">The current health of the element.</span></span> <span data-ttu-id="2bb2e-232">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2bb2e-233">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2bb2e-234">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="2bb2e-235">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-235">Value</span></span>                                                                        | <span data-ttu-id="2bb2e-236">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2bb2e-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2bb2e-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="2bb2e-238">Der Integritäts Status ist "Normal".</span><span class="sxs-lookup"><span data-stu-id="2bb2e-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2bb2e-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-240">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-242">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2bb2e-243">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-247">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-248">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2bb2e-249">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-250">**Name**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-253">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-254">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-254">The label by which the object is known.</span></span> <span data-ttu-id="2bb2e-255">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "vssnapsvc" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-256">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-259">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2bb2e-260">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2bb2e-261">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2bb2e-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="2bb2e-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="2bb2e-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2bb2e-281">)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb2e-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-283">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2bb2e-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-285">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-285">The current statuses of the object.</span></span> <span data-ttu-id="2bb2e-286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-287">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-290">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2bb2e-291">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2bb2e-292">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-296">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-297">Alle Informationen dazu, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="2bb2e-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="2bb2e-298">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-299">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-302">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-303">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="2bb2e-304">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="2bb2e-305">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-306">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-307">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-309">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-309">Provides high level status information.</span></span> <span data-ttu-id="2bb2e-310">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2bb2e-311">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2bb2e-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2bb2e-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="2bb2e-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="2bb2e-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2bb2e-319">)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb2e-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-321">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-323">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="2bb2e-324">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2bb2e-325">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="2bb2e-326">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="2bb2e-327">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="2bb2e-328">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="2bb2e-329">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-329">Value</span></span>                                                                         | <span data-ttu-id="2bb2e-330">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2bb2e-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2bb2e-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2bb2e-332">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="2bb2e-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2bb2e-333">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-334">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-336">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="2bb2e-337">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-338">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-339">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-341">Qualifizierer: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-342">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="2bb2e-343">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-344">**Status**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-347">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-348">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-349">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2bb2e-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-351">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2bb2e-352">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "der Dienst wird normal ausgeführt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-353">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-354">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-356">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-357">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-357">The scoping system's creation class name.</span></span> <span data-ttu-id="2bb2e-358">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-359">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-362">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-363">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="2bb2e-364">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-365">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-366">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-368">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2bb2e-369">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2bb2e-370">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb2e-371">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bb2e-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bb2e-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb2e-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bb2e-373">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2bb2e-374">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2bb2e-375">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="2bb2e-376">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2bb2e-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2bb2e-377"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2bb2e-378"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2bb2e-379"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="2bb2e-380"><dt>**Herunterfahren**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="2bb2e-381"><dt>**Keine Änderung**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="2bb2e-382">Es wird kein Übergang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="2bb2e-383"><dt>**Offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="2bb2e-384"><dt>**Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="2bb2e-385"><dt></dt> Zurückstellen <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="2bb2e-386"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="2bb2e-387"><dt>**Neustart**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="2bb2e-388"><dt>11</dt> <dt>**Zurücksetzen**</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2bb2e-389"><dt>**Nicht zutreffend**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="2bb2e-390">Die-Implementierung unterstützt das darstellen von laufenden Übergängen nicht.</span><span class="sxs-lookup"><span data-stu-id="2bb2e-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="2bb2e-391"><dt> **DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bb2e-392">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bb2e-392">Requirements</span></span>



| <span data-ttu-id="2bb2e-393">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bb2e-393">Requirement</span></span> | <span data-ttu-id="2bb2e-394">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb2e-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb2e-395">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-395">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb2e-396">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb2e-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2bb2e-397">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bb2e-397">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb2e-398">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb2e-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bb2e-399">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bb2e-399">Namespace</span></span><br/>                | <span data-ttu-id="2bb2e-400">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2bb2e-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2bb2e-401">MOF</span><span class="sxs-lookup"><span data-stu-id="2bb2e-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bb2e-402"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bb2e-403">DLL</span><span class="sxs-lookup"><span data-stu-id="2bb2e-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bb2e-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2bb2e-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

