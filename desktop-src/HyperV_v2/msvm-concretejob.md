---
description: Stellt eine Arbeitseinheit dar und wird verwendet, um den Fortschritt von asynchronen Vorgängen zu verfolgen.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Msvm_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356257"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="469f1-103">MSVM- \_ Klasse "concretejob"</span><span class="sxs-lookup"><span data-stu-id="469f1-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="469f1-104">Eine konkrete Version des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="469f1-104">A concrete version of job.</span></span> <span data-ttu-id="469f1-105">Diese Klasse stellt eine generische und Instanzierbare Arbeitseinheit dar, z. b. einen Batch oder einen Druckauftrag, und wird in Hyper-V speziell verwendet, um den Fortschritt von asynchronen Vorgängen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="469f1-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="469f1-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="469f1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="469f1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="469f1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="469f1-108">Member</span><span class="sxs-lookup"><span data-stu-id="469f1-108">Members</span></span>

<span data-ttu-id="469f1-109">Die **MSVM-Klasse " \_ concretejob** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="469f1-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="469f1-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="469f1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="469f1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="469f1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="469f1-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="469f1-112">Methods</span></span>

<span data-ttu-id="469f1-113">Die **MSVM-Klasse " \_ concretejob** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="469f1-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="469f1-114">Methode</span><span class="sxs-lookup"><span data-stu-id="469f1-114">Method</span></span>                                                            | <span data-ttu-id="469f1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="469f1-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="469f1-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="469f1-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="469f1-117">Ruft das Fehler Objekt für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="469f1-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="469f1-118">**Geterrorex**</span><span class="sxs-lookup"><span data-stu-id="469f1-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="469f1-119">Ruft die Fehler Objekte für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="469f1-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="469f1-120">**Killjob**</span><span class="sxs-lookup"><span data-stu-id="469f1-120">**KillJob**</span></span>                                                       | <span data-ttu-id="469f1-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="469f1-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="469f1-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="469f1-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="469f1-123">Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="469f1-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="469f1-124">Properties</span></span>

<span data-ttu-id="469f1-125">Die **MSVM-Klasse " \_ concretejob** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="469f1-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="469f1-126">**Abbrechbar**</span><span class="sxs-lookup"><span data-stu-id="469f1-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="469f1-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-129">Gibt an, ob der Auftrag abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="469f1-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="469f1-130">Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="469f1-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="469f1-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-134">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="469f1-134">A short description of the object.</span></span> <span data-ttu-id="469f1-135">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-136">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="469f1-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-139">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="469f1-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="469f1-140">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="469f1-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-142">**Deleteoncompletion**</span><span class="sxs-lookup"><span data-stu-id="469f1-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="469f1-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-145">Gibt an, ob der Auftrag nach Abschluss des Vorgangs automatisch gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="469f1-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="469f1-146">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="469f1-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-150">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="469f1-150">A description of the object.</span></span> <span data-ttu-id="469f1-151">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="469f1-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-155">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="469f1-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="469f1-156">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="469f1-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-158">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="469f1-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-159">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-161">Das Zeitintervall, in dem der Auftrag ausgeführt wurde, oder die Gesamt Ausführungszeit, wenn der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="469f1-162">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="469f1-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-166">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="469f1-166">A display name for the object.</span></span> <span data-ttu-id="469f1-167">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="469f1-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-169">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-171">Ein Hersteller spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="469f1-171">A vendor-specific error code.</span></span> <span data-ttu-id="469f1-172">Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="469f1-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="469f1-173">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="469f1-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-177">Eine Zeichenfolge, die die Hersteller Fehlerbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="469f1-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="469f1-178">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="469f1-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="469f1-182">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="469f1-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="469f1-183">Eine zusammenfassende Beschreibung des Fehlers, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="469f1-183">A summary description of the error, if present.</span></span> <span data-ttu-id="469f1-184">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="469f1-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-186">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-188">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="469f1-188">The current health of the element.</span></span> <span data-ttu-id="469f1-189">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="469f1-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="469f1-190">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="469f1-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="469f1-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="469f1-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="469f1-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-193">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-195">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="469f1-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="469f1-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="469f1-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="469f1-200">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="469f1-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="469f1-201">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="469f1-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="469f1-202">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="469f1-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="469f1-203">**Jobruntimes**</span><span class="sxs-lookup"><span data-stu-id="469f1-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-204">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="469f1-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-206">Gibt an, wie oft der Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="469f1-206">The number of times that the job should be run.</span></span> <span data-ttu-id="469f1-207">Der Wert 1 gibt an, dass der Auftrag nicht wiederholt wird, während ein Wert ungleich NULL einen Grenzwert für die Häufigkeit angibt, mit der der Auftrag wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="469f1-208">NULL gibt an, dass es keine Beschränkung gibt, wie oft der Auftrag verarbeitet werden kann. er wird jedoch entweder beendet, nachdem die **untilzeit** erreicht wurde, oder der Auftrag wird manuell beendet.</span><span class="sxs-lookup"><span data-stu-id="469f1-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="469f1-209">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="469f1-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-213">**Jobstate** ist eine ganzzahlige Enumeration, die den Betriebszustand eines Auftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="469f1-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="469f1-214">Sie kann auch die Übergänge zwischen diesen Zuständen angeben, z. b. "Herunterfahren" und "starten".</span><span class="sxs-lookup"><span data-stu-id="469f1-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="469f1-215">Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="469f1-216">Wert</span><span class="sxs-lookup"><span data-stu-id="469f1-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="469f1-217">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="469f1-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="469f1-218"><dt>**Neu**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="469f1-219">Der Auftrag wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="469f1-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="469f1-220"><dt>**Ab**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="469f1-221">Der Auftrag wechselt von den Zuständen 2 (neu), 5 (angehalten) oder 11 (Dienst) in den Zustand 4 (wird ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="469f1-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="469f1-222"><dt>**Ausführen**</dt> von <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="469f1-223">Der Auftrag wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="469f1-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="469f1-224"><dt></dt> Angehalten <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="469f1-225">Der Auftrag wurde angehalten, kann jedoch nahtlos neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="469f1-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="469f1-226"><dt>**Herunter**</dt> fahren <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="469f1-227">Der Auftrag wechselt in den Status 7 (abgeschlossen), 8 (beendet) oder 9 (abgebrochen).</span><span class="sxs-lookup"><span data-stu-id="469f1-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="469f1-228"><dt>**Abgeschlossen**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="469f1-229">Der Auftrag wurde normal abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="469f1-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="469f1-230"><dt>**Beendet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="469f1-231">Der Auftrag wurde mit dem Status "beenden" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="469f1-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="469f1-232">Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="469f1-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="469f1-233">Die Anforderung, dass der Auftrag nur dann neu gestartet werden soll, wenn ein neuer Auftrag für die auftragsspezifische Aufgabe gilt.</span><span class="sxs-lookup"><span data-stu-id="469f1-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="469f1-234"><dt></dt> <dt>9</dt> abgebrochen</span><span class="sxs-lookup"><span data-stu-id="469f1-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="469f1-235">Der Auftrag wurde mit dem Status "Kill" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="469f1-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="469f1-236">Zugrunde liegende Prozesse können weiterhin ausgeführt werden, und es ist möglicherweise ein Cleanup erforderlich, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="469f1-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="469f1-237"><dt>**Ausnahme**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="469f1-238">Der Auftrag befindet sich in einem nicht ordnungsgemäßen Zustand, der möglicherweise auf eine Fehlerbedingung hinweist.</span><span class="sxs-lookup"><span data-stu-id="469f1-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="469f1-239">Der tatsächliche Status des Auftrags ist möglicherweise über auftragsspezifische Objekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="469f1-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="469f1-240"><dt>**Dienst**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="469f1-241">Der Auftrag befindet sich in einem herstellerspezifischen Zustand, der die Problem Ermittlung oder-Lösung oder beides unterstützt.</span><span class="sxs-lookup"><span data-stu-id="469f1-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="469f1-242"><dt>**DMTF reserviert**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="469f1-243">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="469f1-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="469f1-244"><dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="469f1-245">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="469f1-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="469f1-246">**Auftragsstatus**</span><span class="sxs-lookup"><span data-stu-id="469f1-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-249">Eine Zeichenfolge, die den Auftragsstatus darstellt.</span><span class="sxs-lookup"><span data-stu-id="469f1-249">A string that represents the job status.</span></span> <span data-ttu-id="469f1-250">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="469f1-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-252">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-254">Gibt den Typ des Auftrags an, der von diesem-Objekt nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="469f1-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="469f1-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Virtuellen Computer definieren** (1)</span><span class="sxs-lookup"><span data-stu-id="469f1-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Virtuellen Computer ändern** (2)</span><span class="sxs-lookup"><span data-stu-id="469f1-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Virtuellen Computer zerstören** (3)</span><span class="sxs-lookup"><span data-stu-id="469f1-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="469f1-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Ändern von Verwaltungsdienst Einstellungen** (4)</span><span class="sxs-lookup"><span data-stu-id="469f1-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Virtuellen Computer initialisieren** (10)</span><span class="sxs-lookup"><span data-stu-id="469f1-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Auf den Start der virtuellen Maschine wird gewartet** (11)</span><span class="sxs-lookup"><span data-stu-id="469f1-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Virtuellen Computer starten** (12)</span><span class="sxs-lookup"><span data-stu-id="469f1-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Virtuellen Computer ausschalten** (13)</span><span class="sxs-lookup"><span data-stu-id="469f1-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Virtuellen Computer speichern** (14)</span><span class="sxs-lookup"><span data-stu-id="469f1-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Virtuellen Computer wiederherstellen** (15)</span><span class="sxs-lookup"><span data-stu-id="469f1-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Virtuellen Computer herunter** fahren (16)</span><span class="sxs-lookup"><span data-stu-id="469f1-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Virtuellen Computer** anhalten (26)</span><span class="sxs-lookup"><span data-stu-id="469f1-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Virtuellen Computer** fortsetzen (27)</span><span class="sxs-lookup"><span data-stu-id="469f1-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Virtuellen Computer zurücksetzen** (28)</span><span class="sxs-lookup"><span data-stu-id="469f1-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Virtuellen Computer neu starten** (29)</span><span class="sxs-lookup"><span data-stu-id="469f1-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="469f1-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Ressourcen für virtuelle Computer hinzufügen** (30)</span><span class="sxs-lookup"><span data-stu-id="469f1-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="469f1-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Ändern der Ressourcen virtueller Computer** (31)</span><span class="sxs-lookup"><span data-stu-id="469f1-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="469f1-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Entfernen von Ressourcen für virtuelle Computer** (32)</span><span class="sxs-lookup"><span data-stu-id="469f1-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="469f1-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Anfänglichen Arbeitsspeicher für virtuelle Maschinen anfordern** (40)</span><span class="sxs-lookup"><span data-stu-id="469f1-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>Arbeits **Speicher zum virtuellen Computer hinzufügen** (41)</span><span class="sxs-lookup"><span data-stu-id="469f1-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>Arbeits **Speicher aus dem virtuellen Computer entfernen** (42)</span><span class="sxs-lookup"><span data-stu-id="469f1-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="469f1-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>Zusammenführen von **VHD** -Datenträgern (50)</span><span class="sxs-lookup"><span data-stu-id="469f1-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Erstellen einer VSS-Momentaufnahme innerhalb eines virtuellen** Computers (51)</span><span class="sxs-lookup"><span data-stu-id="469f1-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="469f1-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Importieren von Import Einstellungsdaten** (60)</span><span class="sxs-lookup"><span data-stu-id="469f1-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Virtuellen Computer importieren** (61)</span><span class="sxs-lookup"><span data-stu-id="469f1-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Virtuellen Computer exportieren** (62)</span><span class="sxs-lookup"><span data-stu-id="469f1-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="469f1-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Konfiguration** (63)</span><span class="sxs-lookup"><span data-stu-id="469f1-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="469f1-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Aufhebung der Registrierung der Konfiguration** (64)</span><span class="sxs-lookup"><span data-stu-id="469f1-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Virtueller Snapshot-Computer** (70)</span><span class="sxs-lookup"><span data-stu-id="469f1-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="469f1-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Momentaufnahme des virtuellen Computers anwenden** (71)</span><span class="sxs-lookup"><span data-stu-id="469f1-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="469f1-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Momentaufnahme des virtuellen Computers löschen** (72)</span><span class="sxs-lookup"><span data-stu-id="469f1-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="469f1-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Momentaufnahme Status der virtuellen Maschine löschen** (73)</span><span class="sxs-lookup"><span data-stu-id="469f1-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="469f1-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Ressourcen zum Ressourcen Pool hinzufügen** (80)</span><span class="sxs-lookup"><span data-stu-id="469f1-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="469f1-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Entfernen von Ressourcen aus dem Ressourcen Pool** (81)</span><span class="sxs-lookup"><span data-stu-id="469f1-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="469f1-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Ändern der Replikations Server Einstellungen** (90)</span><span class="sxs-lookup"><span data-stu-id="469f1-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="469f1-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Replikations Beziehung erstellen** (91)</span><span class="sxs-lookup"><span data-stu-id="469f1-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="469f1-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Ändern der Einstellungen für die Replikations Beziehung** (92)</span><span class="sxs-lookup"><span data-stu-id="469f1-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="469f1-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Replikations Beziehung entfernen** (93)</span><span class="sxs-lookup"><span data-stu-id="469f1-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="469f1-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Starten der ersten Inband-Replikation** (94)</span><span class="sxs-lookup"><span data-stu-id="469f1-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="469f1-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Importieren der Replikation** (95)</span><span class="sxs-lookup"><span data-stu-id="469f1-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="469f1-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Statusänderung replizieren** (96)</span><span class="sxs-lookup"><span data-stu-id="469f1-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="469f1-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiieren eines Failovers** (97)</span><span class="sxs-lookup"><span data-stu-id="469f1-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="469f1-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Failover** wiederherstellen (98)</span><span class="sxs-lookup"><span data-stu-id="469f1-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="469f1-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit-Failover** (99)</span><span class="sxs-lookup"><span data-stu-id="469f1-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="469f1-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Initialisieren der Synchronisierungs Replikation** (100)</span><span class="sxs-lookup"><span data-stu-id="469f1-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="469f1-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Synchronizierte Replikation Abbrechen** (101)</span><span class="sxs-lookup"><span data-stu-id="469f1-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="469f1-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiieren des Test Replikats** (102)</span><span class="sxs-lookup"><span data-stu-id="469f1-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="469f1-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Test Replikat entfernen** (103)</span><span class="sxs-lookup"><span data-stu-id="469f1-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="469f1-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Umgekehrte Replikation** (104)</span><span class="sxs-lookup"><span data-stu-id="469f1-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="469f1-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replikations Sende Delta** (105)</span><span class="sxs-lookup"><span data-stu-id="469f1-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="469f1-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replikations Empfangs Delta** (106)</span><span class="sxs-lookup"><span data-stu-id="469f1-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="469f1-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Neusynchronisierung** (107)</span><span class="sxs-lookup"><span data-stu-id="469f1-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="469f1-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Änderungsprotokoll anwenden** (108)</span><span class="sxs-lookup"><span data-stu-id="469f1-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="469f1-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Anfängliche Replikation Abbrechen** (109)</span><span class="sxs-lookup"><span data-stu-id="469f1-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="469f1-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Neusynchronisierung Abbrechen** (110)</span><span class="sxs-lookup"><span data-stu-id="469f1-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="469f1-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Replikat Statistiken erhalten** (111)</span><span class="sxs-lookup"><span data-stu-id="469f1-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="469f1-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Vorbereiten der Konsistenz** Prüfung (112)</span><span class="sxs-lookup"><span data-stu-id="469f1-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="469f1-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Konsistenz** Prüfung (113)</span><span class="sxs-lookup"><span data-stu-id="469f1-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="469f1-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Konsistenzprüfung Abbrechen** (114)</span><span class="sxs-lookup"><span data-stu-id="469f1-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="469f1-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replikations Verbindung** (115)</span><span class="sxs-lookup"><span data-stu-id="469f1-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="469f1-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Senden des ersten Replikats** (116)</span><span class="sxs-lookup"><span data-stu-id="469f1-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="469f1-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Neusynchronisierung der ersten Replikation starten** (117)</span><span class="sxs-lookup"><span data-stu-id="469f1-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="469f1-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Anfängliche Export-Replikation starten** (118)</span><span class="sxs-lookup"><span data-stu-id="469f1-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="469f1-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Replikat Statistik zurücksetzen** (119)</span><span class="sxs-lookup"><span data-stu-id="469f1-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="469f1-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Registrierte Delta anwenden** (120)</span><span class="sxs-lookup"><span data-stu-id="469f1-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="469f1-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Neusynchronisierung der erweiterten Replikation** (121)</span><span class="sxs-lookup"><span data-stu-id="469f1-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="469f1-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Lesen der Test Replikat Konfiguration** (122)</span><span class="sxs-lookup"><span data-stu-id="469f1-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="469f1-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Ändern des Replikations Modus in "primär** " (123)</span><span class="sxs-lookup"><span data-stu-id="469f1-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="469f1-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Failback initiieren** (124)</span><span class="sxs-lookup"><span data-stu-id="469f1-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="469f1-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>Datenträger **Satz aktualisieren** (125)</span><span class="sxs-lookup"><span data-stu-id="469f1-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-326">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="469f1-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Ethernet-Switch definieren** (130)</span><span class="sxs-lookup"><span data-stu-id="469f1-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="469f1-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Ändern der Ethernet-Switcheinstellungen** (131)</span><span class="sxs-lookup"><span data-stu-id="469f1-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="469f1-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Ethernet-Switch zerstören** (132)</span><span class="sxs-lookup"><span data-stu-id="469f1-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="469f1-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Hinzufügen von Ethernet-switchressourcen** (133)</span><span class="sxs-lookup"><span data-stu-id="469f1-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="469f1-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Ändern von Ethernet-switchressourcen** (134)</span><span class="sxs-lookup"><span data-stu-id="469f1-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="469f1-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Entfernen von Ethernet-switchressourcen** (135)</span><span class="sxs-lookup"><span data-stu-id="469f1-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Geplanten virtuellen Computer** überprüfen (140)</span><span class="sxs-lookup"><span data-stu-id="469f1-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>Der **virtuelle Computer wird erkannt** (141).</span><span class="sxs-lookup"><span data-stu-id="469f1-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="469f1-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Erstellen eines Ressourcenpools** (150)</span><span class="sxs-lookup"><span data-stu-id="469f1-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="469f1-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Ändern der übergeordneten Ressourcen eines Ressourcenpools** (151)</span><span class="sxs-lookup"><span data-stu-id="469f1-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="469f1-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Ändern der Einstellungen für die nichtzuweisung eines Ressourcenpools** (152)</span><span class="sxs-lookup"><span data-stu-id="469f1-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="469f1-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Löschen eines Ressourcenpools** (153)</span><span class="sxs-lookup"><span data-stu-id="469f1-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="469f1-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Remotefx-GPU aktivieren** (160)</span><span class="sxs-lookup"><span data-stu-id="469f1-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="469f1-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Remotefx-GPU deaktivieren** (161)</span><span class="sxs-lookup"><span data-stu-id="469f1-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="469f1-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Ändern der Einstellungen für den 3D-Dienst** (162)</span><span class="sxs-lookup"><span data-stu-id="469f1-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-342">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="469f1-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Virtuellen Computer sichern** (170)</span><span class="sxs-lookup"><span data-stu-id="469f1-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="469f1-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Gast Dienst Schnittstelle** (180)</span><span class="sxs-lookup"><span data-stu-id="469f1-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-345">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="469f1-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Gast Cluster Informationen Abfragen** (181)</span><span class="sxs-lookup"><span data-stu-id="469f1-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-347">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="469f1-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Sammlung definieren** (190)</span><span class="sxs-lookup"><span data-stu-id="469f1-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-349">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="469f1-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Sammlung zerstören** (191)</span><span class="sxs-lookup"><span data-stu-id="469f1-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-351">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="469f1-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Sammlung umbenennen** (192)</span><span class="sxs-lookup"><span data-stu-id="469f1-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-353">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="469f1-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Mitglied zur Sammlung hinzufügen** (193)</span><span class="sxs-lookup"><span data-stu-id="469f1-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-355">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="469f1-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Mitglied aus Sammlung entfernen** (194)</span><span class="sxs-lookup"><span data-stu-id="469f1-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-357">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="469f1-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Einstellung zu Sammlung hinzufügen** (195)</span><span class="sxs-lookup"><span data-stu-id="469f1-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-359">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="469f1-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Einstellung aus Sammlung entfernen** (196)</span><span class="sxs-lookup"><span data-stu-id="469f1-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-361">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="469f1-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Einstellung für Sammlung ändern** (197)</span><span class="sxs-lookup"><span data-stu-id="469f1-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-363">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="469f1-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Momentaufnahme Sammlung** (198)</span><span class="sxs-lookup"><span data-stu-id="469f1-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-365">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="469f1-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Momentaufnahme in Verweis Punkt konvertieren** (200)</span><span class="sxs-lookup"><span data-stu-id="469f1-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-367">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="469f1-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Erstellen eines Bezugspunkts** (201)</span><span class="sxs-lookup"><span data-stu-id="469f1-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-369">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="469f1-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Verweis Punkt löschen** (202)</span><span class="sxs-lookup"><span data-stu-id="469f1-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-371">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="469f1-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Referenzpunkt** (203)</span><span class="sxs-lookup"><span data-stu-id="469f1-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-373">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="469f1-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Entfernen der zugeordneten Daten aus dem Referenzpunkt** (204)</span><span class="sxs-lookup"><span data-stu-id="469f1-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-375">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="469f1-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Referenzpunkt für Sammlung erstellen** (205)</span><span class="sxs-lookup"><span data-stu-id="469f1-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-377">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="469f1-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Verweis Punkt in Sammlung** (206)</span><span class="sxs-lookup"><span data-stu-id="469f1-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-379">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="469f1-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Verknüpfte Daten aus Referenzpunkt in Sammlung entfernen** (207)</span><span class="sxs-lookup"><span data-stu-id="469f1-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-381">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="469f1-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Verweis Punkt in Sammlung löschen** (208)</span><span class="sxs-lookup"><span data-stu-id="469f1-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-383">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="469f1-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Importieren von Verweis Punkt Metadaten** (209)</span><span class="sxs-lookup"><span data-stu-id="469f1-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-385">Der in Windows 10 als **cleanupverweispunkt** hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="469f1-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>Bereitstellung von **Zustell barem Gerät einbinden oder** aufheben (260)</span><span class="sxs-lookup"><span data-stu-id="469f1-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="469f1-387">Der in Windows 10 hinzugefügte Wert.</span><span class="sxs-lookup"><span data-stu-id="469f1-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="469f1-388">**Localorutctime**</span><span class="sxs-lookup"><span data-stu-id="469f1-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-389">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-391">Gibt an, ob die in den Eigenschaften **runstartinterval** und **UntilTime** dargestellten Uhrzeiten Ortszeit oder UTC-Zeiten darstellen.</span><span class="sxs-lookup"><span data-stu-id="469f1-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="469f1-392">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="469f1-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ortszeit** (1)</span><span class="sxs-lookup"><span data-stu-id="469f1-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC-Zeit** (2)</span><span class="sxs-lookup"><span data-stu-id="469f1-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="469f1-395">**Name**</span><span class="sxs-lookup"><span data-stu-id="469f1-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-396">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="469f1-398">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="469f1-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="469f1-399">Der Anzeige Name für diese Instanz eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="469f1-399">The display name for this instance of a job.</span></span> <span data-ttu-id="469f1-400">Außerdem kann der Anzeige Name als Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="469f1-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="469f1-401">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-402">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="469f1-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-405">Der Benutzer, der nach Abschluss oder Fehler des Auftrags benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="469f1-406">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-407">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="469f1-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-408">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-410">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="469f1-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="469f1-411">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="469f1-412">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="469f1-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-414">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="469f1-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="469f1-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-416">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="469f1-416">The current statuses of the object.</span></span> <span data-ttu-id="469f1-417">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="469f1-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-418">**Otherherstellyaction**</span><span class="sxs-lookup"><span data-stu-id="469f1-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-419">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-421">Eine Zeichenfolge, die die Wiederherstellungs Aktion beschreibt, wenn die **Wiederherstellungs Action** -Eigenschaft der-Instanz 1 (Sonstiges) ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="469f1-422">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-423">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="469f1-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-426">Der Benutzer, der den Auftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="469f1-426">The user who submitted the job.</span></span> <span data-ttu-id="469f1-427">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="469f1-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-429">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="469f1-431">Qualifizierer: **MinValue** (0), **MaxValue** (100), **Units** ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="469f1-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="469f1-432">Der Abschluss Prozentsatz des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="469f1-432">The completion percentage of the job.</span></span> <span data-ttu-id="469f1-433">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-434">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="469f1-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-435">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-437">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="469f1-437">Provides high level status information.</span></span> <span data-ttu-id="469f1-438">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="469f1-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="469f1-439">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="469f1-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="469f1-440">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-441">**Priority**</span><span class="sxs-lookup"><span data-stu-id="469f1-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-442">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="469f1-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-444">Die Wichtigkeit der Ausführung eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="469f1-444">The importance of a job's execution.</span></span> <span data-ttu-id="469f1-445">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-446">**Wiederherstellbarkeits Aktion**</span><span class="sxs-lookup"><span data-stu-id="469f1-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-447">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="469f1-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-449">Beschreibt die Wiederherstellungs Aktion, die für einen Auftrag ausgeführt werden soll, der nicht erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="469f1-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="469f1-450">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="469f1-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="469f1-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="469f1-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortsetzen** (2)</span><span class="sxs-lookup"><span data-stu-id="469f1-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Fortfahren mit dem nächsten Auftrag** (3)</span><span class="sxs-lookup"><span data-stu-id="469f1-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)</span><span class="sxs-lookup"><span data-stu-id="469f1-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Wiederherstellungsauftrag ausführen** (5)</span><span class="sxs-lookup"><span data-stu-id="469f1-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="469f1-457">**Runday**</span><span class="sxs-lookup"><span data-stu-id="469f1-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-458">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="469f1-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="469f1-460">Qualifizierer: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="469f1-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="469f1-461">Der Tag des Monats, an dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469f1-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="469f1-462">Abhängig vom Wert von **rundayosweek** gibt es unterschiedliche Interpretationen für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="469f1-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="469f1-463">Wenn **rundayosweek** den Wert 0 hat und **runday** positiv ist, definiert **runday** den Tag des Monats, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="469f1-464">Wenn **rundayosweek** beispielsweise 0 und **runday** 12 ist, wird der Auftrag am 12 <sup>.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="469f1-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="469f1-465">Wenn **rundayosweek** 0 und **runday** negativ ist, definiert **runday** die Anzahl von Tagen vor dem letzten Tag des Monats, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="469f1-466">1 gibt den letzten Tag des Monats an, 2 gibt einen Tag vor dem letzten Tag des Monats an usw.</span><span class="sxs-lookup"><span data-stu-id="469f1-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="469f1-467">Wenn **rundayosweek** beispielsweise 0 und **runday** 1 ist, wird der Auftrag am letzten Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="469f1-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="469f1-468">Wenn **rundayofweek** nicht 0 ist, ist **rundayofweek** der Wochentag, an dem der Auftrag im Verhältnis zum **runday** verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="469f1-469">Wenn **runday** beispielsweise 15 und **rundayosweek** 7 (+ Samstag) ist, wird der Auftrag am ersten Samstag am oder nach <sup>dem 15.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="469f1-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="469f1-470">Wenn **runday** den Wert 20 hat und **rundayosweek** 7 (Samstag) ist, wird der Auftrag am ersten Samstag am oder vor <sup>dem 20.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="469f1-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="469f1-471">Wenn **runday** 1 und **rundayosweek** 1 (Sonntag) ist, wird der Auftrag am letzten Sonntag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="469f1-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="469f1-472">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-473">**Rundayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="469f1-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-474">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="469f1-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-476">Eine positive oder negative ganze Zahl, die zusammen mit **runday** zum Angeben des Wochentags oder Monats, an dem der Auftrag verarbeitet wird, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="469f1-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="469f1-477">Weitere Informationen finden Sie in der Beschreibung der **runday** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="469f1-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="469f1-478">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="469f1-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="469f1-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="469f1-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="469f1-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="469f1-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="469f1-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="469f1-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="469f1-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Exactdayosmonth** (0)</span><span class="sxs-lookup"><span data-stu-id="469f1-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="469f1-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="469f1-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="469f1-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="469f1-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="469f1-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="469f1-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="469f1-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="469f1-494">**Runmonth**</span><span class="sxs-lookup"><span data-stu-id="469f1-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-495">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="469f1-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-496">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-497">Der Monat, in dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469f1-497">The month during which the job should be processed.</span></span> <span data-ttu-id="469f1-498">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="469f1-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Januar** (0)</span><span class="sxs-lookup"><span data-stu-id="469f1-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Februar** (1)</span><span class="sxs-lookup"><span data-stu-id="469f1-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**März** (2)</span><span class="sxs-lookup"><span data-stu-id="469f1-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span><span class="sxs-lookup"><span data-stu-id="469f1-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="469f1-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juni** (5)</span><span class="sxs-lookup"><span data-stu-id="469f1-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Juli** (6)</span><span class="sxs-lookup"><span data-stu-id="469f1-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span><span class="sxs-lookup"><span data-stu-id="469f1-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span><span class="sxs-lookup"><span data-stu-id="469f1-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Oktober** (9)</span><span class="sxs-lookup"><span data-stu-id="469f1-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span><span class="sxs-lookup"><span data-stu-id="469f1-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="469f1-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezember** (11)</span><span class="sxs-lookup"><span data-stu-id="469f1-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="469f1-511">**Runstartinterval**</span><span class="sxs-lookup"><span data-stu-id="469f1-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-512">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-514">Das Zeitintervall nach Mitternacht, zu dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469f1-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="469f1-515">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-516">**Scheduledstarttime**</span><span class="sxs-lookup"><span data-stu-id="469f1-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-517">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-518">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-519">Die geplante Startzeit für den Auftrag, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="469f1-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="469f1-520">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-522">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-523">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-524">Der Zeitpunkt, zu dem der Auftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="469f1-524">The time that the job began.</span></span> <span data-ttu-id="469f1-525">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-526">**Status**</span><span class="sxs-lookup"><span data-stu-id="469f1-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-527">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="469f1-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-528">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-529">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="469f1-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="469f1-530">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="469f1-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-531">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="469f1-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="469f1-532">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-533">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="469f1-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="469f1-534">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="469f1-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="469f1-535">**Timebeforeremoval**</span><span class="sxs-lookup"><span data-stu-id="469f1-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-536">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-537">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-538">Die Zeitspanne (in Minuten), die der Auftrag nach Abschluss der Ausführung aufbewahrt wird, entweder erfolgreich oder Fehler in dieser Ausführung.</span><span class="sxs-lookup"><span data-stu-id="469f1-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="469f1-539">Der Auftrag muss für einige Zeit vorhanden sein, unabhängig vom Wert der **deleteoncompletion** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="469f1-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="469f1-540">Der Standardwert beträgt fünf Minuten.</span><span class="sxs-lookup"><span data-stu-id="469f1-540">The default is five minutes.</span></span> <span data-ttu-id="469f1-541">Diese Eigenschaft wird von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))geerbt und ist immer auf 00000000000500.000000:000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="469f1-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="469f1-542">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="469f1-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-543">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-544">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-545">Das Datum oder die Uhrzeit der letzten Änderung des Auftrags Zustands.</span><span class="sxs-lookup"><span data-stu-id="469f1-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="469f1-546">Wenn der Status des Auftrags nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="469f1-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="469f1-547">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="469f1-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="469f1-548">Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-549">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="469f1-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-550">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-551">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-552">Der Zeitpunkt, zu dem der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="469f1-552">The time that the job was submitted.</span></span> <span data-ttu-id="469f1-553">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="469f1-554">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="469f1-555">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="469f1-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="469f1-556">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469f1-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="469f1-557">Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="469f1-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="469f1-558">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="469f1-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="469f1-559">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="469f1-559">Remarks</span></span>

<span data-ttu-id="469f1-560">Der Zugriff auf die **MSVM-Klasse " \_ concretejob** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="469f1-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="469f1-561">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="469f1-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="469f1-562">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="469f1-562">Requirements</span></span>



| <span data-ttu-id="469f1-563">Anforderung</span><span class="sxs-lookup"><span data-stu-id="469f1-563">Requirement</span></span> | <span data-ttu-id="469f1-564">Wert</span><span class="sxs-lookup"><span data-stu-id="469f1-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="469f1-565">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="469f1-565">Minimum supported client</span></span><br/> | <span data-ttu-id="469f1-566">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="469f1-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="469f1-567">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="469f1-567">Minimum supported server</span></span><br/> | <span data-ttu-id="469f1-568">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="469f1-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="469f1-569">Namespace</span><span class="sxs-lookup"><span data-stu-id="469f1-569">Namespace</span></span><br/>                | <span data-ttu-id="469f1-570">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="469f1-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="469f1-571">MOF</span><span class="sxs-lookup"><span data-stu-id="469f1-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="469f1-572"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="469f1-573">DLL</span><span class="sxs-lookup"><span data-stu-id="469f1-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="469f1-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="469f1-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="469f1-575">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="469f1-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469f1-576">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="469f1-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="469f1-577">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="469f1-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="469f1-578">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="469f1-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

