---
description: MSVM \_ guestservice ist die abstrakte Basisklasse für Dienste im Gast, auf die vom Host zugegriffen werden kann.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Msvm_GuestService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393430"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="46938-103">MSVM \_ guestservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="46938-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="46938-104">**MSVM \_ Guestservice** ist die abstrakte Basisklasse für Dienste im Gast, auf die vom Host zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="46938-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="46938-105">Diese Klasse wird von der [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service) Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="46938-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="46938-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="46938-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46938-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="46938-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="46938-108">Member</span><span class="sxs-lookup"><span data-stu-id="46938-108">Members</span></span>

<span data-ttu-id="46938-109">Die **MSVM \_ guestservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="46938-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="46938-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="46938-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="46938-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46938-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="46938-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="46938-112">Methods</span></span>

<span data-ttu-id="46938-113">Die **MSVM \_ guestservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="46938-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="46938-114">Methode</span><span class="sxs-lookup"><span data-stu-id="46938-114">Method</span></span>                                                             | <span data-ttu-id="46938-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46938-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46938-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="46938-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="46938-117">Fordert an, dass der Zustand des Gast Diensts auf den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="46938-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="46938-118">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="46938-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="46938-119">Versetzt den Gast Dienst in den Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="46938-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="46938-120">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="46938-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="46938-121">Beendet den Gast Dienst.</span><span class="sxs-lookup"><span data-stu-id="46938-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="46938-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46938-122">Properties</span></span>

<span data-ttu-id="46938-123">Die **MSVM \_ guestservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46938-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46938-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="46938-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-127">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="46938-127">Short textual description of the object.</span></span> <span data-ttu-id="46938-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46938-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="46938-129">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="46938-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-132">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46938-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="46938-133">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="46938-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="46938-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46938-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-137">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46938-137">Textual description of the object.</span></span> <span data-ttu-id="46938-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46938-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="46938-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46938-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="46938-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46938-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-142">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="46938-142">Date and time the object was installed.</span></span> <span data-ttu-id="46938-143">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="46938-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="46938-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46938-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="46938-145">**Name**</span><span class="sxs-lookup"><span data-stu-id="46938-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-148">Eindeutiger Bezeichner für den Dienst, der auch eine Angabe der verwalteten Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="46938-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="46938-149">Weitere Informationen zu den Funktionen finden Sie in der **Description** -Eigenschaft des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46938-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="46938-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46938-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="46938-151">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="46938-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-152">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="46938-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46938-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-154">**True** gibt an, dass der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="46938-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="46938-155">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="46938-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-158">Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="46938-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="46938-159">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="46938-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="46938-160">**Schem**</span><span class="sxs-lookup"><span data-stu-id="46938-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="46938-161">**Manual**</span><span class="sxs-lookup"><span data-stu-id="46938-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46938-162">**Status**</span><span class="sxs-lookup"><span data-stu-id="46938-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-165">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46938-165">Current status of the object.</span></span> <span data-ttu-id="46938-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46938-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="46938-167">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="46938-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="46938-168">**Okay**</span><span class="sxs-lookup"><span data-stu-id="46938-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="46938-169">**Zeit**</span><span class="sxs-lookup"><span data-stu-id="46938-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="46938-170">**Zerstört**</span><span class="sxs-lookup"><span data-stu-id="46938-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="46938-171">**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="46938-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="46938-172">**"Pred Fail"**</span><span class="sxs-lookup"><span data-stu-id="46938-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="46938-173">**Fahren**</span><span class="sxs-lookup"><span data-stu-id="46938-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="46938-174">**Hindern**</span><span class="sxs-lookup"><span data-stu-id="46938-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="46938-175">**Leistungs**</span><span class="sxs-lookup"><span data-stu-id="46938-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="46938-176">**Gestresst**</span><span class="sxs-lookup"><span data-stu-id="46938-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="46938-177">**"Nicht wiederherstellen"**</span><span class="sxs-lookup"><span data-stu-id="46938-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="46938-178">**"Kein Kontakt"**</span><span class="sxs-lookup"><span data-stu-id="46938-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="46938-179">**"Verlorene comm"**</span><span class="sxs-lookup"><span data-stu-id="46938-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46938-180">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="46938-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-183">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="46938-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="46938-184">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="46938-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46938-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46938-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46938-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46938-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46938-187">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="46938-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46938-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46938-188">Requirements</span></span>



| <span data-ttu-id="46938-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46938-189">Requirement</span></span> | <span data-ttu-id="46938-190">Wert</span><span class="sxs-lookup"><span data-stu-id="46938-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46938-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46938-191">Minimum supported client</span></span><br/> | <span data-ttu-id="46938-192">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="46938-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="46938-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46938-193">Minimum supported server</span></span><br/> | <span data-ttu-id="46938-194">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46938-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="46938-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="46938-195">Namespace</span></span><br/>                | <span data-ttu-id="46938-196">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="46938-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46938-197">MOF</span><span class="sxs-lookup"><span data-stu-id="46938-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46938-198"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46938-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46938-199">DLL</span><span class="sxs-lookup"><span data-stu-id="46938-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46938-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46938-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46938-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46938-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46938-202">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="46938-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="46938-203">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="46938-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

