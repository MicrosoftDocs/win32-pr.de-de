---
description: Diese Klasse stellt einen Migrations Vorgangs Auftrag dar, der für die Migration des virtuellen System Migrations Dienstanbieter oder des virtuellen Systems erstellt wurde.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Msvm_MigrationJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372963"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="fe4e4-103">MSVM \_ migrationjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe4e4-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="fe4e4-104">Diese Klasse stellt einen Migrations Vorgangs Auftrag dar, der für die Migration des virtuellen System Migrations Dienstanbieter oder des virtuellen Systems erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="fe4e4-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe4e4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
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
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="fe4e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="fe4e4-107">Members</span></span>

<span data-ttu-id="fe4e4-108">Die **MSVM \_ migrationjob** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe4e4-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="fe4e4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="fe4e4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe4e4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe4e4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fe4e4-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fe4e4-111">Methods</span></span>

<span data-ttu-id="fe4e4-112">Die **MSVM \_ migrationjob** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="fe4e4-113">Methode</span><span class="sxs-lookup"><span data-stu-id="fe4e4-113">Method</span></span>                                                             | <span data-ttu-id="fe4e4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe4e4-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe4e4-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="fe4e4-116">Ruft das Fehler Objekt für den Migrations Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="fe4e4-117">**Geterrorex**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="fe4e4-118">Ruft die Fehler Objekte für den Migrations Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="fe4e4-119">**Killjob**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-119">**KillJob**</span></span>                                                        | <span data-ttu-id="fe4e4-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="fe4e4-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="fe4e4-122">Fordert an, dass der Status des Migrations Auftrags in den angegebenen Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fe4e4-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe4e4-123">Properties</span></span>

<span data-ttu-id="fe4e4-124">Die **MSVM \_ migrationjob** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe4e4-125">**Abbrechbar**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fe4e4-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-128">Gibt an, ob der Auftrag abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="fe4e4-129">Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-133">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-133">A short description of the object.</span></span> <span data-ttu-id="fe4e4-134">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-135">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-136">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-138">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="fe4e4-139">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fe4e4-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-141">**Deleteoncompletion**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fe4e4-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-144">Gibt an, ob der Auftrag nach Abschluss des Vorgangs automatisch gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="fe4e4-145">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-149">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-149">A description of the object.</span></span> <span data-ttu-id="fe4e4-150">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-151">**Destinationhost**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-154">Der Hostname der zielvirtualisierungsplattform, zu der das virtuelle System migriert wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="fe4e4-155">Dieser Wert wird für die Speicher Migration **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-159">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="fe4e4-160">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fe4e4-161">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-162">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-163">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-165">Das Zeitintervall, in dem der Auftrag ausgeführt wurde, oder die Gesamt Ausführungszeit, wenn der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="fe4e4-166">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-170">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-170">A display name for the object.</span></span> <span data-ttu-id="fe4e4-171">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-175">Ein Hersteller spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-175">A vendor-specific error code.</span></span> <span data-ttu-id="fe4e4-176">Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="fe4e4-177">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-181">Eine Zeichenfolge, die die Hersteller Fehlerbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="fe4e4-182">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-186">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="fe4e4-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-187">Eine zusammenfassende Beschreibung des Fehlers, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-189">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-191">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-191">The current health of the element.</span></span> <span data-ttu-id="fe4e4-192">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="fe4e4-193">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="fe4e4-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-196">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-198">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="fe4e4-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-203">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-204">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fe4e4-205">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-206">**Jobruntimes**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-209">Gibt an, wie oft der Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-209">The number of times that the job should be run.</span></span> <span data-ttu-id="fe4e4-210">Der Wert 1 gibt an, dass der Auftrag nicht wiederholt wird, während ein Wert ungleich NULL einen Grenzwert für die Häufigkeit angibt, mit der der Auftrag wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="fe4e4-211">NULL gibt an, dass es keine Beschränkung gibt, wie oft der Auftrag verarbeitet werden kann. er wird jedoch entweder beendet, nachdem die **untilzeit** erreicht wurde, oder der Auftrag wird manuell beendet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="fe4e4-212">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-214">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-216">**Jobstate** ist eine ganzzahlige Enumeration, die den Betriebszustand eines Auftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="fe4e4-217">Sie kann auch die Übergänge zwischen diesen Zuständen angeben, z. b. "Herunterfahren" und "starten".</span><span class="sxs-lookup"><span data-stu-id="fe4e4-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="fe4e4-218">Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="fe4e4-219">Wert</span><span class="sxs-lookup"><span data-stu-id="fe4e4-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="fe4e4-220">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe4e4-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="fe4e4-221"><dt>**Neu**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="fe4e4-222">Der Auftrag wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="fe4e4-223"><dt>**Ab**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="fe4e4-224">Der Auftrag wechselt von den Zuständen 2 (neu), 5 (angehalten) oder 11 (Dienst) in den Zustand 4 (wird ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="fe4e4-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="fe4e4-225"><dt>**Ausführen**</dt> von <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="fe4e4-226">Der Auftrag wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="fe4e4-227"><dt></dt> Angehalten <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="fe4e4-228">Der Auftrag wurde angehalten, kann jedoch nahtlos neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="fe4e4-229"><dt>**Herunter**</dt> fahren <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="fe4e4-230">Der Auftrag wechselt in den Status 7 (abgeschlossen), 8 (beendet) oder 9 (abgebrochen).</span><span class="sxs-lookup"><span data-stu-id="fe4e4-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="fe4e4-231"><dt>**Abgeschlossen**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="fe4e4-232">Der Auftrag wurde normal abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="fe4e4-233"><dt>**Beendet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="fe4e4-234">Der Auftrag wurde mit dem Status "beenden" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="fe4e4-235">Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="fe4e4-236">Die Anforderung, dass der Auftrag nur dann neu gestartet werden soll, wenn ein neuer Auftrag ein Auftrags spezifischer Auftrag ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="fe4e4-237"><dt></dt> <dt>9</dt> abgebrochen</span><span class="sxs-lookup"><span data-stu-id="fe4e4-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="fe4e4-238">Der Auftrag wurde mit dem Status "Kill" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="fe4e4-239">Zugrunde liegende Prozesse können weiterhin ausgeführt werden, und es ist möglicherweise ein Cleanup erforderlich, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="fe4e4-240"><dt>**Ausnahme**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="fe4e4-241">Der Auftrag befindet sich in einem nicht ordnungsgemäßen Zustand, der möglicherweise auf eine Fehlerbedingung hinweist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="fe4e4-242">Der tatsächliche Status des Auftrags ist möglicherweise über auftragsspezifische Objekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="fe4e4-243"><dt>**Dienst**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="fe4e4-244">Der Auftrag befindet sich in einem herstellerspezifischen Zustand, der die Problem Ermittlung oder-Lösung oder beides unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="fe4e4-245"><dt>**DMTF reserviert**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="fe4e4-246">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="fe4e4-247"><dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="fe4e4-248">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="fe4e4-249">**Auftragsstatus**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-252">Eine Zeichenfolge, die den Auftragsstatus darstellt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-252">A string that represents the job status.</span></span> <span data-ttu-id="fe4e4-253">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-255">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-257">Gibt den Typ des Auftrags an, der von diesem-Objekt nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fe4e4-258">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="fe4e4-259">Der **virtuelle Remote Computer wird erstellt** (300).</span><span class="sxs-lookup"><span data-stu-id="fe4e4-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="fe4e4-260">Über **Prüfen der Kompatibilität der virtuellen Maschine** (301)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="fe4e4-261">Über **Prüfen der Kompatibilität virtueller Computer und Speicher** (302)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="fe4e4-262">Über **Prüfen der Speicher Kompatibilität** (303)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="fe4e4-263">Über **Prüfen der Speicher Migration** (304)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="fe4e4-264">**Verschieben des virtuellen** Computers (305)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="fe4e4-265">**Verschieben von virtuellen Maschinen und Speicher** (306)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="fe4e4-266">**Verschieben von Speicher** (307)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fe4e4-267">**Localorutctime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-268">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-270">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="fe4e4-271">Gibt an, ob die in den Eigenschaften **runstartinterval** und **UntilTime** dargestellten Uhrzeiten Ortszeit oder UTC-Zeiten darstellen.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="fe4e4-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ortszeit** (1)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC-Zeit** (2)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe4e4-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-275">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-277">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md)".**MigrationType**")</span><span class="sxs-lookup"><span data-stu-id="fe4e4-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-278">Der durch dieses Auftrags Objekt dargestellte Migrationstyp.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-278">The migration type represented by this job object.</span></span> <span data-ttu-id="fe4e4-279">Dies ist einer der Werte, die für die **migrationType** -Eigenschaft der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-280">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-283">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-284">Der Anzeige Name für diese Instanz eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-284">The display name for this instance of a job.</span></span> <span data-ttu-id="fe4e4-285">Außerdem kann der Anzeige Name als Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="fe4e4-286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-287">**Newresourcesettingdata**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-288">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fe4e4-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-290">Bei einer Live Migration wird dies immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="fe4e4-291">Bei einer Speicher Migration werden die virtuellen Festplatten (VHDs) der virtuellen Maschine verschoben, wenn diese **null** ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="fe4e4-292">Andernfalls enthält dies ein Array von eingebetteten Instanzen der Klasse " [**MSVM \_ storagezudationsettingdata**](msvm-storageallocationsettingdata.md) ", die die zu verschieben VHDs darstellen.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="fe4e4-293">Mit der **Connection** -Eigenschaft dieser Instanzen wird der Ziel Speicherort der virtuellen Festplatte angegeben.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-294">**Newsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-297">Bei einer Live Migration wird dies immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="fe4e4-298">Bei einer Speicher Migration werden die Daten Stämme der virtuellen Maschine nicht verschoben, wenn diese **null** ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="fe4e4-299">Andernfalls enthält Sie eine eingebettete Instanz der [**MSVM-Klasse " \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) ", bei der die Eigenschaften " **externaldataroot**", " **snapshotdataroot**" und " **tauapfiledataroot** " die neuen Daten Stämme angeben.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-300">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-303">Der Benutzer, der nach Abschluss oder Fehler des Auftrags benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="fe4e4-304">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-305">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-306">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-308">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="fe4e4-309">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fe4e4-310">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-312">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="fe4e4-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-314">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-314">The current statuses of the object.</span></span> <span data-ttu-id="fe4e4-315">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-316">**Otherherstellyaction**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-319">Eine Zeichenfolge, die die Wiederherstellungs Aktion beschreibt, wenn die **Wiederherstellungs Action** -Eigenschaft der-Instanz 1 (Sonstiges) ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="fe4e4-320">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-321">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-324">Der Benutzer, der den Auftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-324">The user who submitted the job.</span></span> <span data-ttu-id="fe4e4-325">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-327">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-329">Qualifizierer: **MinValue** (0), **MaxValue** (100), **Units** ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="fe4e4-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-330">Der Abschluss Prozentsatz des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-330">The completion percentage of the job.</span></span> <span data-ttu-id="fe4e4-331">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-332">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-333">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-335">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-335">Provides high level status information.</span></span> <span data-ttu-id="fe4e4-336">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="fe4e4-337">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fe4e4-338">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-339">**Priority**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-340">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-342">Die Wichtigkeit der Ausführung eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-342">The importance of a job's execution.</span></span> <span data-ttu-id="fe4e4-343">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-344">**Wiederherstellbarkeits Aktion**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-345">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-347">Beschreibt die Wiederherstellungs Aktion, die für einen erfolglos ausgeführten Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="fe4e4-348">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="fe4e4-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortsetzen** (2)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Fortfahren mit dem nächsten Auftrag** (3)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Wiederherstellungsauftrag ausführen** (5)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe4e4-355">**Runday**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-356">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-358">Qualifizierer: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-359">Der Tag des Monats, an dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="fe4e4-360">Abhängig vom Wert von **rundayosweek** gibt es unterschiedliche Interpretationen für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="fe4e4-361">Wenn **rundayosweek** den Wert 0 hat und **runday** positiv ist, definiert **runday** den Tag des Monats, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="fe4e4-362">Wenn **rundayosweek** beispielsweise 0 und **runday** 12 ist, wird der Auftrag am 12 <sup>.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="fe4e4-363">Wenn **rundayosweek** 0 und **runday** negativ ist, definiert **runday** die Anzahl von Tagen vor dem letzten Tag des Monats, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="fe4e4-364">1 gibt den letzten Tag des Monats an, 2 gibt einen Tag vor dem letzten Tag des Monats an usw.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="fe4e4-365">Wenn **rundayosweek** beispielsweise 0 und **runday** 1 ist, wird der Auftrag am letzten Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="fe4e4-366">Wenn **rundayofweek** nicht 0 ist, ist **rundayofweek** der Wochentag, an dem der Auftrag im Verhältnis zum **runday** verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="fe4e4-367">Wenn **runday** beispielsweise 15 und **rundayosweek** 7 (+ Samstag) ist, wird der Auftrag am ersten Samstag am oder nach <sup>dem 15.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="fe4e4-368">Wenn **runday** den Wert 20 hat und **rundayosweek** 7 (Samstag) ist, wird der Auftrag am ersten Samstag am oder vor <sup>dem 20.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="fe4e4-369">Wenn **runday** 1 und **rundayosweek** 1 (Sonntag) ist, wird der Auftrag am letzten Sonntag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="fe4e4-370">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-371">**Rundayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-372">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-374">Eine positive oder negative ganze Zahl, die zusammen mit **runday** zum Angeben des Wochentags oder Monats, an dem der Auftrag verarbeitet wird, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="fe4e4-375">Weitere Informationen finden Sie in der Beschreibung der **runday** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="fe4e4-376">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="fe4e4-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Exactdayosmonth** (0)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe4e4-392">**Runmonth**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-393">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-395">Der Monat, in dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-395">The month during which the job should be processed.</span></span> <span data-ttu-id="fe4e4-396">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="fe4e4-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Januar** (0)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Februar** (1)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**März** (2)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juni** (5)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Juli** (6)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Oktober** (9)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezember** (11)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe4e4-409">**Runstartinterval**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-410">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-412">Das Zeitintervall nach Mitternacht, zu dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="fe4e4-413">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-414">**Scheduledstarttime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-415">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-417">Die geplante Startzeit für den Auftrag, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="fe4e4-418">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-420">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-422">Der Zeitpunkt, zu dem der Auftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-422">The time that the job began.</span></span> <span data-ttu-id="fe4e4-423">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-424">**Status**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-425">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-427">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-428">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-429">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fe4e4-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-431">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="fe4e4-432">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-433">**Timebeforeremoval**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-434">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-436">Die Zeitspanne (in Minuten), die der Auftrag nach Abschluss der Ausführung aufbewahrt wird, entweder erfolgreich oder Fehler in dieser Ausführung.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="fe4e4-437">Der Auftrag muss für einige Zeit vorhanden sein, unabhängig vom Wert der **deleteoncompletion** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="fe4e4-438">Der Standardwert beträgt fünf Minuten.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-438">The default is five minutes.</span></span> <span data-ttu-id="fe4e4-439">Diese Eigenschaft wird von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))geerbt und ist immer auf 00000000000500.000000:000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-440">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-441">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-443">Das Datum oder die Uhrzeit der letzten Änderung des Auftrags Zustands.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="fe4e4-444">Wenn der Status des Auftrags nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="fe4e4-445">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="fe4e4-446">Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-447">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-448">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-450">Der Zeitpunkt, zu dem der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-450">The time that the job was submitted.</span></span> <span data-ttu-id="fe4e4-451">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-452">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-453">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-455">Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="fe4e4-456">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="fe4e4-457">**Virtualsystemname**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe4e4-458">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe4e4-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe4e4-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe4e4-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe4e4-460">Der eindeutige Name des betroffenen virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="fe4e4-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe4e4-461">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe4e4-461">Requirements</span></span>



| <span data-ttu-id="fe4e4-462">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe4e4-462">Requirement</span></span> | <span data-ttu-id="fe4e4-463">Wert</span><span class="sxs-lookup"><span data-stu-id="fe4e4-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4e4-464">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-464">Minimum supported client</span></span><br/> | <span data-ttu-id="fe4e4-465">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe4e4-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fe4e4-466">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe4e4-466">Minimum supported server</span></span><br/> | <span data-ttu-id="fe4e4-467">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe4e4-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe4e4-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe4e4-468">Namespace</span></span><br/>                | <span data-ttu-id="fe4e4-469">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fe4e4-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe4e4-470">MOF</span><span class="sxs-lookup"><span data-stu-id="fe4e4-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe4e4-471"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe4e4-472">DLL</span><span class="sxs-lookup"><span data-stu-id="fe4e4-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe4e4-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e4-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

