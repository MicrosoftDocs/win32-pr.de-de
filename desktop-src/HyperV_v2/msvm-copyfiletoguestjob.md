---
description: Stellt einen Gast Datei Dienst-Vorgangs Auftrag dar.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Msvm_CopyFileToGuestJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363568"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="4727e-103">MSVM \_ copyfiledeguestjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="4727e-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="4727e-104">Stellt einen Gast Datei Dienst-Vorgangs Auftrag dar.</span><span class="sxs-lookup"><span data-stu-id="4727e-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="4727e-105">Diese Klasse wird von [**MSVM \_ guestfileservice**](msvm-guestfileservice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4727e-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="4727e-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="4727e-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4727e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4727e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
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
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="4727e-108">Member</span><span class="sxs-lookup"><span data-stu-id="4727e-108">Members</span></span>

<span data-ttu-id="4727e-109">Die **MSVM \_ copyfiletoguestjob** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4727e-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="4727e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="4727e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4727e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4727e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4727e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4727e-112">Methods</span></span>

<span data-ttu-id="4727e-113">Die **MSVM \_ copyfiledeguestjob** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4727e-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="4727e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="4727e-114">Method</span></span>                                                                   | <span data-ttu-id="4727e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4727e-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="4727e-116">**Copyfilestoguest**</span><span class="sxs-lookup"><span data-stu-id="4727e-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="4727e-117">Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="4727e-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="4727e-118">**GetError**</span><span class="sxs-lookup"><span data-stu-id="4727e-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="4727e-119">Ruft das Fehler Objekt für den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4727e-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="4727e-120">**Geterrorex**</span><span class="sxs-lookup"><span data-stu-id="4727e-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="4727e-121">Ruft die Fehler Objekte für den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4727e-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="4727e-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4727e-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="4727e-123">Ändert den Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="4727e-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="4727e-124">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="4727e-124">**StartService**</span></span>                                                         | <span data-ttu-id="4727e-125">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4727e-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="4727e-126">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="4727e-126">**StopService**</span></span>                                                          | <span data-ttu-id="4727e-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4727e-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="4727e-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4727e-128">Properties</span></span>

<span data-ttu-id="4727e-129">Die **MSVM \_ copyfiledeguestjob** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4727e-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4727e-130">**Abbrechbar**</span><span class="sxs-lookup"><span data-stu-id="4727e-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-131">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4727e-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-133">Gibt an, ob der Auftrag abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4727e-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="4727e-134">Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4727e-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="4727e-135">**True** gibt an, dass der Auftrag abgebrochen werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="4727e-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4727e-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4727e-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-139">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4727e-139">Short textual description of the object.</span></span> <span data-ttu-id="4727e-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4727e-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4727e-141">**Copyfilestarguestsettingdata**</span><span class="sxs-lookup"><span data-stu-id="4727e-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-142">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4727e-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4727e-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-144">Festlegen von Daten, die zum Kopieren einer Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4727e-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="4727e-145">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4727e-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-148">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4727e-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4727e-149">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4727e-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="4727e-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4727e-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-153">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4727e-153">Textual description of the object.</span></span> <span data-ttu-id="4727e-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4727e-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4727e-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="4727e-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4727e-158">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="4727e-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="4727e-159">Eine zusammenfassende Beschreibung des Fehlers, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4727e-159">A summary description of the error, if present.</span></span> <span data-ttu-id="4727e-160">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4727e-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4727e-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4727e-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-162">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4727e-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-164">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4727e-164">Date and time the object was installed.</span></span> <span data-ttu-id="4727e-165">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4727e-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="4727e-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4727e-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4727e-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="4727e-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-170">Eindeutiger Bezeichner für den Dienst, der auch eine Angabe der verwalteten Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4727e-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="4727e-171">Weitere Informationen zu den Funktionen finden Sie in der **Description** -Eigenschaft des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4727e-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="4727e-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4727e-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4727e-173">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="4727e-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-174">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4727e-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-176">**True** gibt an, dass der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4727e-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="4727e-177">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4727e-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-180">Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4727e-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="4727e-181">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4727e-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="4727e-182">**Schem**</span><span class="sxs-lookup"><span data-stu-id="4727e-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="4727e-183">**Manual**</span><span class="sxs-lookup"><span data-stu-id="4727e-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4727e-184">**Status**</span><span class="sxs-lookup"><span data-stu-id="4727e-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-187">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4727e-187">Current status of the object.</span></span> <span data-ttu-id="4727e-188">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4727e-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="4727e-189">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4727e-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="4727e-190">**Okay**</span><span class="sxs-lookup"><span data-stu-id="4727e-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="4727e-191">**Zeit**</span><span class="sxs-lookup"><span data-stu-id="4727e-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="4727e-192">**Zerstört**</span><span class="sxs-lookup"><span data-stu-id="4727e-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="4727e-193">**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="4727e-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="4727e-194">**"Pred Fail"**</span><span class="sxs-lookup"><span data-stu-id="4727e-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="4727e-195">**Fahren**</span><span class="sxs-lookup"><span data-stu-id="4727e-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="4727e-196">**Hindern**</span><span class="sxs-lookup"><span data-stu-id="4727e-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="4727e-197">**Leistungs**</span><span class="sxs-lookup"><span data-stu-id="4727e-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="4727e-198">**Gestresst**</span><span class="sxs-lookup"><span data-stu-id="4727e-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="4727e-199">**"Nicht wiederherstellen"**</span><span class="sxs-lookup"><span data-stu-id="4727e-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="4727e-200">**"Kein Kontakt"**</span><span class="sxs-lookup"><span data-stu-id="4727e-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="4727e-201">**"Verlorene comm"**</span><span class="sxs-lookup"><span data-stu-id="4727e-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4727e-202">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="4727e-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-205">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4727e-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="4727e-206">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="4727e-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-209">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="4727e-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="4727e-210">**Virtualsystemname**</span><span class="sxs-lookup"><span data-stu-id="4727e-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4727e-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4727e-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4727e-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4727e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4727e-213">GUID des betroffenen virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="4727e-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4727e-214">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4727e-214">Requirements</span></span>



| <span data-ttu-id="4727e-215">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4727e-215">Requirement</span></span> | <span data-ttu-id="4727e-216">Wert</span><span class="sxs-lookup"><span data-stu-id="4727e-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4727e-217">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4727e-217">Minimum supported client</span></span><br/> | <span data-ttu-id="4727e-218">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="4727e-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4727e-219">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4727e-219">Minimum supported server</span></span><br/> | <span data-ttu-id="4727e-220">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4727e-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4727e-221">Namespace</span><span class="sxs-lookup"><span data-stu-id="4727e-221">Namespace</span></span><br/>                | <span data-ttu-id="4727e-222">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4727e-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4727e-223">MOF</span><span class="sxs-lookup"><span data-stu-id="4727e-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4727e-224"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4727e-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4727e-225">DLL</span><span class="sxs-lookup"><span data-stu-id="4727e-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4727e-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4727e-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4727e-227">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4727e-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4727e-228">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="4727e-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="4727e-229">**MSVM \_ guestfileservice**</span><span class="sxs-lookup"><span data-stu-id="4727e-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="4727e-230">**MSVM- \_ guestservice**</span><span class="sxs-lookup"><span data-stu-id="4727e-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

