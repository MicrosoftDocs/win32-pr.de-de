---
description: MSVM \_ guestfileservice enthält eine Methode, die zum Kopieren einer Datei auf eine virtuelle Maschine vom Hyper-V-Host verwendet werden kann.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Msvm_GuestFileService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342829"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="0c604-103">MSVM \_ guestfileservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0c604-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="0c604-104">**MSVM \_ Guestfileservice** enthält eine Methode, die verwendet werden kann, um eine Datei auf einen virtuellen Computer vom Hyper-V-Host zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0c604-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="0c604-105">Diese Klasse wird von [**MSVM \_ guestservice**](msvm-guestservice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0c604-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="0c604-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0c604-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c604-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c604-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
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

## <a name="members"></a><span data-ttu-id="0c604-108">Member</span><span class="sxs-lookup"><span data-stu-id="0c604-108">Members</span></span>

<span data-ttu-id="0c604-109">Die **MSVM \_ guestfileservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0c604-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="0c604-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0c604-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c604-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c604-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c604-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0c604-112">Methods</span></span>

<span data-ttu-id="0c604-113">Die **MSVM \_ guestfileservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0c604-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="0c604-114">Methode</span><span class="sxs-lookup"><span data-stu-id="0c604-114">Method</span></span>                                                             | <span data-ttu-id="0c604-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c604-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c604-116">**Copyfilestoguest**</span><span class="sxs-lookup"><span data-stu-id="0c604-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="0c604-117">Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="0c604-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="0c604-118">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c604-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="0c604-119">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="0c604-119">**StartService**</span></span>                                                   | <span data-ttu-id="0c604-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c604-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="0c604-121">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="0c604-121">**StopService**</span></span>                                                    | <span data-ttu-id="0c604-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c604-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="0c604-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c604-123">Properties</span></span>

<span data-ttu-id="0c604-124">Die **MSVM \_ guestfileservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0c604-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c604-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0c604-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-128">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c604-128">Short textual description of the object.</span></span> <span data-ttu-id="0c604-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c604-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c604-130">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0c604-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-133">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c604-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0c604-134">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0c604-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="0c604-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c604-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-138">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c604-138">Textual description of the object.</span></span> <span data-ttu-id="0c604-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c604-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c604-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0c604-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-141">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c604-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-143">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c604-143">Date and time the object was installed.</span></span> <span data-ttu-id="0c604-144">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c604-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="0c604-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c604-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c604-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="0c604-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-149">Eindeutiger Bezeichner für den Dienst, der auch eine Angabe der verwalteten Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0c604-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="0c604-150">Weitere Informationen zu den Funktionen finden Sie in der **Description** -Eigenschaft des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c604-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="0c604-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c604-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c604-152">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="0c604-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-153">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0c604-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-155">**True** gibt an, dass der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="0c604-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="0c604-156">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0c604-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-159">Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0c604-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="0c604-160">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="0c604-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="0c604-161">**Schem**</span><span class="sxs-lookup"><span data-stu-id="0c604-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="0c604-162">**Manual**</span><span class="sxs-lookup"><span data-stu-id="0c604-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c604-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="0c604-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-166">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c604-166">Current status of the object.</span></span> <span data-ttu-id="0c604-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c604-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="0c604-168">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="0c604-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="0c604-169">**Okay**</span><span class="sxs-lookup"><span data-stu-id="0c604-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="0c604-170">**Zeit**</span><span class="sxs-lookup"><span data-stu-id="0c604-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="0c604-171">**Zerstört**</span><span class="sxs-lookup"><span data-stu-id="0c604-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="0c604-172">**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="0c604-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="0c604-173">**"Pred Fail"**</span><span class="sxs-lookup"><span data-stu-id="0c604-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="0c604-174">**Fahren**</span><span class="sxs-lookup"><span data-stu-id="0c604-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="0c604-175">**Hindern**</span><span class="sxs-lookup"><span data-stu-id="0c604-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="0c604-176">**Leistungs**</span><span class="sxs-lookup"><span data-stu-id="0c604-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="0c604-177">**Gestresst**</span><span class="sxs-lookup"><span data-stu-id="0c604-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="0c604-178">**"Nicht wiederherstellen"**</span><span class="sxs-lookup"><span data-stu-id="0c604-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="0c604-179">**"Kein Kontakt"**</span><span class="sxs-lookup"><span data-stu-id="0c604-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="0c604-180">**"Verlorene comm"**</span><span class="sxs-lookup"><span data-stu-id="0c604-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c604-181">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="0c604-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-184">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="0c604-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="0c604-185">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="0c604-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c604-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c604-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c604-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c604-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c604-188">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="0c604-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c604-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c604-189">Requirements</span></span>



| <span data-ttu-id="0c604-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c604-190">Requirement</span></span> | <span data-ttu-id="0c604-191">Wert</span><span class="sxs-lookup"><span data-stu-id="0c604-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c604-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c604-192">Minimum supported client</span></span><br/> | <span data-ttu-id="0c604-193">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0c604-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0c604-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c604-194">Minimum supported server</span></span><br/> | <span data-ttu-id="0c604-195">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c604-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0c604-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c604-196">Namespace</span></span><br/>                | <span data-ttu-id="0c604-197">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0c604-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c604-198">MOF</span><span class="sxs-lookup"><span data-stu-id="0c604-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c604-199"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0c604-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c604-200">DLL</span><span class="sxs-lookup"><span data-stu-id="0c604-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c604-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c604-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c604-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c604-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c604-203">**MSVM- \_ guestservice**</span><span class="sxs-lookup"><span data-stu-id="0c604-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

