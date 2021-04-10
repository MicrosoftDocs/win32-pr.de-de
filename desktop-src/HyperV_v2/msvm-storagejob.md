---
description: Stellt einen Speicher Vorgangs Auftrag dar, der vom Microsoft Hyper-V Abbild Verwaltungsdienst erstellt wurde.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Msvm_StorageJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869083"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="a850c-103">MSVM \_ storagejob-Klasse</span><span class="sxs-lookup"><span data-stu-id="a850c-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="a850c-104">Stellt einen Speicher Vorgangs Auftrag dar, der vom Microsoft Hyper-V Abbild Verwaltungsdienst erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="a850c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a850c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a850c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a850c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="a850c-107">Member</span><span class="sxs-lookup"><span data-stu-id="a850c-107">Members</span></span>

<span data-ttu-id="a850c-108">Die **MSVM \_ storagejob** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a850c-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="a850c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a850c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a850c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a850c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a850c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a850c-111">Methods</span></span>

<span data-ttu-id="a850c-112">Die **MSVM \_ storagejob** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a850c-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="a850c-113">Methode</span><span class="sxs-lookup"><span data-stu-id="a850c-113">Method</span></span>                                                           | <span data-ttu-id="a850c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a850c-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a850c-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="a850c-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="a850c-116">Ruft den Fehler ab, der den Grund für den Fehler des Auftrags beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a850c-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="a850c-117">**Geterrorex**</span><span class="sxs-lookup"><span data-stu-id="a850c-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="a850c-118">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**MSVM- \_ Fehler**](msvm-error.md) Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="a850c-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="a850c-119">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, werden mindestens eine **MSVM- \_ Fehler** Instanz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a850c-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="a850c-120">**Killjob**</span><span class="sxs-lookup"><span data-stu-id="a850c-120">**KillJob**</span></span>                                                      | <span data-ttu-id="a850c-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a850c-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a850c-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a850c-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="a850c-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="a850c-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="a850c-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a850c-124">Properties</span></span>

<span data-ttu-id="a850c-125">Die **MSVM \_ storagejob** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a850c-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a850c-126">**Abbrechbar**</span><span class="sxs-lookup"><span data-stu-id="a850c-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a850c-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-129">Gibt an, ob der Auftrag abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a850c-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="a850c-130">Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a850c-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-134">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a850c-134">A short description of the object.</span></span> <span data-ttu-id="a850c-135">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-136">**Untergeordnet**</span><span class="sxs-lookup"><span data-stu-id="a850c-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-139">Bei einem Fehler des asynchronen Vorgangs enthält diese Eigenschaft den vollständigen Pfad des untergeordneten Elements der VHD, die von diesem Vorgang betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-140">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="a850c-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-143">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a850c-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a850c-144">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a850c-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-146">**Deleteoncompletion**</span><span class="sxs-lookup"><span data-stu-id="a850c-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a850c-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-149">Gibt an, ob der Auftrag nach Abschluss des Vorgangs automatisch gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a850c-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="a850c-150">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a850c-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-154">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a850c-154">A description of the object.</span></span> <span data-ttu-id="a850c-155">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a850c-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-159">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="a850c-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a850c-160">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a850c-161">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-162">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="a850c-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-163">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-165">Die Zeitspanne, für die der Auftrag ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="a850c-166">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a850c-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-170">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a850c-170">A display name for the object.</span></span> <span data-ttu-id="a850c-171">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a850c-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-175">Ein Hersteller spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a850c-175">A vendor-specific error code.</span></span> <span data-ttu-id="a850c-176">Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="a850c-177">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a850c-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-181">Eine Zeichenfolge, die die Hersteller Fehlerbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="a850c-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="a850c-182">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="a850c-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a850c-186">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="a850c-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="a850c-187">Eine zusammenfassende Beschreibung des Fehlers, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a850c-187">A summary description of the error, if present.</span></span> <span data-ttu-id="a850c-188">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a850c-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-192">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="a850c-192">The current health of the element.</span></span> <span data-ttu-id="a850c-193">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a850c-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a850c-194">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a850c-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a850c-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a850c-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-197">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-199">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="a850c-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a850c-200">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a850c-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-204">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a850c-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a850c-205">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-206">**Jobcompletionstatus Code**</span><span class="sxs-lookup"><span data-stu-id="a850c-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a850c-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-209">Der **HRESULT** -Code, der den Abschluss Status für den asynchronen Vorgang beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a850c-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-210">**Jobruntimes**</span><span class="sxs-lookup"><span data-stu-id="a850c-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-211">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a850c-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-213">Gibt an, wie oft der Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a850c-213">The number of times that the job should be run.</span></span> <span data-ttu-id="a850c-214">Der Wert 1 gibt an, dass der Auftrag nicht wiederholt wird, während ein Wert ungleich NULL einen Grenzwert für die Häufigkeit angibt, mit der der Auftrag wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="a850c-215">NULL gibt an, dass es keine Beschränkung gibt, wie oft der Auftrag verarbeitet werden kann. er wird jedoch entweder beendet, nachdem die **untilzeit** erreicht wurde, oder der Auftrag wird manuell beendet.</span><span class="sxs-lookup"><span data-stu-id="a850c-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="a850c-216">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="a850c-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-218">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-220">Der Betriebszustand eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a850c-220">The operational state of a job.</span></span> <span data-ttu-id="a850c-221">Sie kann auch die Übergänge zwischen diesen Zuständen angeben, z. b. 6 (wird heruntergefahren) und 3 (wird gestartet).</span><span class="sxs-lookup"><span data-stu-id="a850c-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="a850c-222">Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="a850c-223">Wert</span><span class="sxs-lookup"><span data-stu-id="a850c-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="a850c-224">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a850c-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="a850c-225"><dt>**Neu**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="a850c-226">Der Auftrag wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="a850c-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="a850c-227"><dt>**Ab**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="a850c-228">Der Auftrag wechselt von den Zuständen "neu", "angehalten" oder "Dienst" in den Status "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="a850c-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="a850c-229"><dt>**Ausführen**</dt> von <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="a850c-230">Der Auftrag wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a850c-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="a850c-231"><dt></dt> Angehalten <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="a850c-232">Der Auftrag wurde angehalten, kann jedoch nahtlos neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a850c-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="a850c-233"><dt>**Herunter**</dt> fahren <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="a850c-234">Der Auftrag wechselt in den Zustand "abgeschlossen", "beendet" oder "abgebrochen".</span><span class="sxs-lookup"><span data-stu-id="a850c-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="a850c-235"><dt>**Abgeschlossen**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="a850c-236">Der Auftrag wurde normal abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a850c-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="a850c-237"><dt>**Beendet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="a850c-238">Der Auftrag wurde mit dem Status "beenden" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="a850c-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="a850c-239">Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a850c-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="a850c-240">Die Anforderung, dass der Auftrag nur dann neu gestartet werden soll, wenn ein neuer Auftrag ein Auftrags spezifischer Auftrag ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="a850c-241"><dt></dt> <dt>9</dt> abgebrochen</span><span class="sxs-lookup"><span data-stu-id="a850c-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="a850c-242">Der Auftrag wurde mit dem Status "Kill" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="a850c-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="a850c-243">Zugrunde liegende Prozesse können weiterhin ausgeführt werden, und es ist möglicherweise ein Cleanup erforderlich, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a850c-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="a850c-244"><dt>**Ausnahme**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="a850c-245">Der Auftrag befindet sich in einem nicht ordnungsgemäßen Zustand, der möglicherweise auf eine Fehlerbedingung hinweist.</span><span class="sxs-lookup"><span data-stu-id="a850c-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="a850c-246">Der tatsächliche Status des Auftrags ist möglicherweise über auftragsspezifische Objekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a850c-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="a850c-247"><dt>**Dienst**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="a850c-248">Der Auftrag befindet sich in einem herstellerspezifischen Zustand, der die Problem Ermittlung oder-Lösung oder beides unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a850c-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="a850c-249"><dt>**DMTF reserviert**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="a850c-250">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a850c-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="a850c-251"><dt> **Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="a850c-252">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a850c-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="a850c-253">**Auftragsstatus**</span><span class="sxs-lookup"><span data-stu-id="a850c-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-256">Eine Zeichenfolge, die den Auftragsstatus darstellt.</span><span class="sxs-lookup"><span data-stu-id="a850c-256">A string that represents the job status.</span></span> <span data-ttu-id="a850c-257">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="a850c-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-259">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-261">Der Typ des asynchronen Vorgangs, der von dieser **MSVM \_ storagejob**-Instanz nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a850c-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a850c-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="a850c-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD-Erstellung** (1)</span><span class="sxs-lookup"><span data-stu-id="a850c-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-264">Erstellen eines Images virtueller Festplatten (VHD).</span><span class="sxs-lookup"><span data-stu-id="a850c-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="a850c-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Disketten Erstellung** (2)</span><span class="sxs-lookup"><span data-stu-id="a850c-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-266">Erstellen eines virtuellen Disketten Images (VFD).</span><span class="sxs-lookup"><span data-stu-id="a850c-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="a850c-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span><span class="sxs-lookup"><span data-stu-id="a850c-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-268">Komprimieren der Größe eines VHD-Abbilds.</span><span class="sxs-lookup"><span data-stu-id="a850c-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="a850c-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Erweiterung** (4)</span><span class="sxs-lookup"><span data-stu-id="a850c-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-270">Erweitern der Größe eines VHD-Abbilds.</span><span class="sxs-lookup"><span data-stu-id="a850c-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="a850c-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>Wird zusammen **geführt (5** )</span><span class="sxs-lookup"><span data-stu-id="a850c-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-272">Zusammenführen mehrerer VHD-Images zu einem einzelnen Image.</span><span class="sxs-lookup"><span data-stu-id="a850c-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="a850c-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Konvertierung** (6)</span><span class="sxs-lookup"><span data-stu-id="a850c-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-274">Der Typ eines virtuellen Festplatten Abbilds wird umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="a850c-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="a850c-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback einbinden** (7)</span><span class="sxs-lookup"><span data-stu-id="a850c-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-276">Einbinden der virtuellen Festplatte auf der übergeordneten Partition</span><span class="sxs-lookup"><span data-stu-id="a850c-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="a850c-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**VHD-Informationen erhalten** (8)</span><span class="sxs-lookup"><span data-stu-id="a850c-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a850c-278">Einbinden der VHD auf dem Verwaltungs Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="a850c-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="a850c-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**VHD-Abbild** überprüfen (9)</span><span class="sxs-lookup"><span data-stu-id="a850c-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a850c-280">**Localorutctime**</span><span class="sxs-lookup"><span data-stu-id="a850c-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-281">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-283">Gibt an, ob die in den Eigenschaften **runstartinterval** und **UntilTime** dargestellten Uhrzeiten Ortszeit oder UTC-Zeiten darstellen.</span><span class="sxs-lookup"><span data-stu-id="a850c-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="a850c-284">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="a850c-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ortszeit** (1)</span><span class="sxs-lookup"><span data-stu-id="a850c-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC-Zeit** (2)</span><span class="sxs-lookup"><span data-stu-id="a850c-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a850c-287">**Name**</span><span class="sxs-lookup"><span data-stu-id="a850c-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-290">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-290">The label by which the object is known.</span></span> <span data-ttu-id="a850c-291">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-292">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="a850c-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-295">Der Benutzer, der nach Abschluss oder Fehler des Auftrags benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="a850c-296">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-297">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="a850c-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-298">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-300">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a850c-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a850c-301">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a850c-302">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a850c-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-304">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a850c-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a850c-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-306">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a850c-306">The current statuses of the object.</span></span> <span data-ttu-id="a850c-307">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-308">**Otherherstellyaction**</span><span class="sxs-lookup"><span data-stu-id="a850c-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-311">Eine Zeichenfolge, die die Wiederherstellungs Aktion beschreibt, wenn die **Wiederherstellungs Action** -Eigenschaft der-Instanz 1 (Sonstiges) ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="a850c-312">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-313">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="a850c-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-316">Der Benutzer, der den Auftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="a850c-316">The user who submitted the job.</span></span> <span data-ttu-id="a850c-317">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-318">**Parent**</span><span class="sxs-lookup"><span data-stu-id="a850c-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-321">Bei einem Fehler des asynchronen Vorgangs enthält diese Eigenschaft den Dateipfad zum übergeordneten Element der VHD, die von diesem Vorgang betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="a850c-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-323">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a850c-325">Qualifizierer: **MinValue** (0), **MaxValue** (100), **Units** ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="a850c-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="a850c-326">Der Abschluss Prozentsatz des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a850c-326">The completion percentage of the job.</span></span> <span data-ttu-id="a850c-327">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-328">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="a850c-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-329">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-331">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="a850c-331">Provides high level status information.</span></span> <span data-ttu-id="a850c-332">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a850c-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a850c-333">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a850c-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a850c-334">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-335">**Priority**</span><span class="sxs-lookup"><span data-stu-id="a850c-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-336">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a850c-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-338">Die Wichtigkeit der Ausführung eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a850c-338">The importance of a job's execution.</span></span> <span data-ttu-id="a850c-339">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-340">**Wiederherstellbarkeits Aktion**</span><span class="sxs-lookup"><span data-stu-id="a850c-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-341">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a850c-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-343">Beschreibt die Wiederherstellungs Aktion, die für einen Auftrag ausgeführt werden soll, der nicht erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="a850c-344">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="a850c-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a850c-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a850c-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortsetzen** (2)</span><span class="sxs-lookup"><span data-stu-id="a850c-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Fortfahren mit dem nächsten Auftrag** (3)</span><span class="sxs-lookup"><span data-stu-id="a850c-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)</span><span class="sxs-lookup"><span data-stu-id="a850c-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Wiederherstellungsauftrag ausführen** (5)</span><span class="sxs-lookup"><span data-stu-id="a850c-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a850c-351">**Runday**</span><span class="sxs-lookup"><span data-stu-id="a850c-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-352">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a850c-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a850c-354">Qualifizierer: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="a850c-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="a850c-355">Der Tag des Monats, an dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a850c-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="a850c-356">Abhängig vom Wert von **rundayosweek** gibt es unterschiedliche Interpretationen für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a850c-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="a850c-357">Wenn **rundayosweek** den Wert 0 hat und **runday** positiv ist, definiert **runday** den Tag des Monats, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="a850c-358">Wenn **rundayosweek** beispielsweise 0 und **runday** 12 ist, wird der Auftrag am 12 <sup>.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a850c-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="a850c-359">Wenn **rundayosweek** 0 und **runday** negativ ist, definiert **runday** die Anzahl von Tagen vor dem letzten Tag des Monats, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="a850c-360">1 gibt den letzten Tag des Monats an, 2 gibt einen Tag vor dem letzten Tag des Monats an usw.</span><span class="sxs-lookup"><span data-stu-id="a850c-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="a850c-361">Wenn **rundayosweek** beispielsweise 0 und **runday** 1 ist, wird der Auftrag am letzten Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a850c-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="a850c-362">Wenn **rundayofweek** nicht 0 ist, ist **rundayofweek** der Wochentag, an dem der Auftrag im Verhältnis zum **runday** verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="a850c-363">Wenn **runday** beispielsweise 15 und **rundayosweek** 7 (+ Samstag) ist, wird der Auftrag am ersten Samstag am oder nach <sup>dem 15.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a850c-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="a850c-364">Wenn **runday** den Wert 20 hat und **rundayosweek** 7 (Samstag) ist, wird der Auftrag am ersten Samstag am oder vor <sup>dem 20.</sup> Tag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a850c-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="a850c-365">Wenn **runday** 1 und **rundayosweek** 1 (Sonntag) ist, wird der Auftrag am letzten Sonntag des Monats verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a850c-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="a850c-366">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-367">**Rundayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="a850c-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-368">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a850c-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-370">Eine positive oder negative ganze Zahl, die zusammen mit **runday** zum Angeben des Wochentags oder Monats, an dem der Auftrag verarbeitet wird, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a850c-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="a850c-371">Weitere Informationen finden Sie in der Beschreibung der **runday** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a850c-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="a850c-372">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="a850c-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="a850c-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="a850c-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="a850c-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="a850c-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="a850c-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="a850c-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="a850c-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Exactdayosmonth** (0)</span><span class="sxs-lookup"><span data-stu-id="a850c-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="a850c-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="a850c-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="a850c-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="a850c-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="a850c-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="a850c-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="a850c-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a850c-388">**Runmonth**</span><span class="sxs-lookup"><span data-stu-id="a850c-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-389">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a850c-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-391">Der Monat, in dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a850c-391">The month during which the job should be processed.</span></span> <span data-ttu-id="a850c-392">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="a850c-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Januar** (0)</span><span class="sxs-lookup"><span data-stu-id="a850c-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Februar** (1)</span><span class="sxs-lookup"><span data-stu-id="a850c-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**März** (2)</span><span class="sxs-lookup"><span data-stu-id="a850c-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span><span class="sxs-lookup"><span data-stu-id="a850c-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="a850c-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juni** (5)</span><span class="sxs-lookup"><span data-stu-id="a850c-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Juli** (6)</span><span class="sxs-lookup"><span data-stu-id="a850c-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span><span class="sxs-lookup"><span data-stu-id="a850c-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span><span class="sxs-lookup"><span data-stu-id="a850c-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Oktober** (9)</span><span class="sxs-lookup"><span data-stu-id="a850c-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span><span class="sxs-lookup"><span data-stu-id="a850c-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a850c-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezember** (11)</span><span class="sxs-lookup"><span data-stu-id="a850c-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a850c-405">**Runstartinterval**</span><span class="sxs-lookup"><span data-stu-id="a850c-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-406">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-408">Das Zeitintervall nach Mitternacht, zu dem der Auftrag verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a850c-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="a850c-409">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-410">**Scheduledstarttime**</span><span class="sxs-lookup"><span data-stu-id="a850c-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-411">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-413">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-415">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-417">Der Zeitpunkt, zu dem der Auftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-417">The time that the job began.</span></span> <span data-ttu-id="a850c-418">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="a850c-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-420">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a850c-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-422">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a850c-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-423">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="a850c-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-424">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a850c-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a850c-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-426">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a850c-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a850c-427">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-428">**Timebeforeremoval**</span><span class="sxs-lookup"><span data-stu-id="a850c-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-429">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-431">Die Zeitspanne (in Minuten), die der Auftrag nach Abschluss der Ausführung aufbewahrt wird, entweder erfolgreich oder Fehler in dieser Ausführung.</span><span class="sxs-lookup"><span data-stu-id="a850c-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="a850c-432">Der Auftrag muss für einige Zeit vorhanden sein, unabhängig vom Wert der **deleteoncompletion** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a850c-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="a850c-433">Der Standardwert beträgt fünf Minuten.</span><span class="sxs-lookup"><span data-stu-id="a850c-433">The default is five minutes.</span></span> <span data-ttu-id="a850c-434">Diese Eigenschaft wird von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))geerbt und ist immer auf 00000000000500.000000:000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a850c-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="a850c-435">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="a850c-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-436">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-438">Der Zeitpunkt, zu dem der Status der virtuellen Maschine zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="a850c-439">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-440">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="a850c-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-441">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-443">Der Zeitpunkt, zu dem der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a850c-443">The time that the job was submitted.</span></span> <span data-ttu-id="a850c-444">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="a850c-445">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a850c-446">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a850c-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a850c-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a850c-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a850c-448">Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="a850c-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="a850c-449">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a850c-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a850c-450">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a850c-450">Remarks</span></span>

<span data-ttu-id="a850c-451">Der Zugriff auf die **MSVM \_ storagejob** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="a850c-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a850c-452">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a850c-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a850c-453">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a850c-453">Requirements</span></span>



| <span data-ttu-id="a850c-454">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a850c-454">Requirement</span></span> | <span data-ttu-id="a850c-455">Wert</span><span class="sxs-lookup"><span data-stu-id="a850c-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a850c-456">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a850c-456">Minimum supported client</span></span><br/> | <span data-ttu-id="a850c-457">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a850c-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a850c-458">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a850c-458">Minimum supported server</span></span><br/> | <span data-ttu-id="a850c-459">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a850c-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a850c-460">Namespace</span><span class="sxs-lookup"><span data-stu-id="a850c-460">Namespace</span></span><br/>                | <span data-ttu-id="a850c-461">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a850c-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a850c-462">MOF</span><span class="sxs-lookup"><span data-stu-id="a850c-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a850c-463"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a850c-464">DLL</span><span class="sxs-lookup"><span data-stu-id="a850c-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a850c-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a850c-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a850c-466">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a850c-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a850c-467">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="a850c-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="a850c-468">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a850c-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a850c-469">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="a850c-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

