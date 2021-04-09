---
description: Ein logisches Element, das eine Arbeitseinheit darstellt, die ausgeführt werden soll, z. b. ein Skript oder ein Druckauftrag. Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant oder in die Warteschlange eingereiht werden kann, und seine Ausführung ist nicht auf ein einzelnes System beschränkt.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960276"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="54c55-104">CIM_Job-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="54c55-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="54c55-105">Ein logisches Element, das eine Arbeitseinheit darstellt, die ausgeführt werden soll, z. b. ein Skript oder ein Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="54c55-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="54c55-106">Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant oder in die Warteschlange eingereiht werden kann, und seine Ausführung ist nicht auf ein einzelnes System beschränkt.</span><span class="sxs-lookup"><span data-stu-id="54c55-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c55-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54c55-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
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
};
```

## <a name="members"></a><span data-ttu-id="54c55-108">Member</span><span class="sxs-lookup"><span data-stu-id="54c55-108">Members</span></span>

<span data-ttu-id="54c55-109">Die **CIM- \_ Auftrags** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="54c55-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="54c55-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="54c55-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="54c55-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54c55-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54c55-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="54c55-112">Methods</span></span>

<span data-ttu-id="54c55-113">Die **CIM- \_ Auftrags** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="54c55-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="54c55-114">Methode</span><span class="sxs-lookup"><span data-stu-id="54c55-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="54c55-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54c55-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="54c55-116"><a href="cim-job-killjob.md"><strong>Killjob</strong></a></span><span class="sxs-lookup"><span data-stu-id="54c55-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="54c55-117">Diese Methode ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="54c55-117">This method is deprecated.</span></span> <span data-ttu-id="54c55-118">Verwenden Sie stattdessen die <strong>requestStateChange</strong> -Methode.</span><span class="sxs-lookup"><span data-stu-id="54c55-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="54c55-119">Veraltete Beschreibung: fährt einen Auftrag herunter.</span><span class="sxs-lookup"><span data-stu-id="54c55-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="54c55-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54c55-120">Properties</span></span>

<span data-ttu-id="54c55-121">Die **CIM- \_ Auftrags** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54c55-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54c55-122">**Deleteoncompletion**</span><span class="sxs-lookup"><span data-stu-id="54c55-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="54c55-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="54c55-125">**True** , um den Auftrag nach dem Abschluss zu löschen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="54c55-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="54c55-126">Diese Eigenschaft löscht keine Aufträge, die beendet werden, bevor diese Eigenschaft auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="54c55-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="54c55-127">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="54c55-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-128">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c55-130">Die Dauer, für die der Auftrag ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="54c55-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="54c55-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-132">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54c55-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-134">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**ErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="54c55-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-135">Ein Hersteller spezifischer Fehlercode, der Verarbeitungs Informationen für wiederkehrende Aufträge erfasst.</span><span class="sxs-lookup"><span data-stu-id="54c55-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="54c55-136">Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="54c55-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="54c55-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54c55-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-140">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="54c55-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-141">Eine frei Form Zeichenfolge, die eine Beschreibung des entsprechenden Fehlercodes in der **errorCode** -Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="54c55-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-142">**Jobruntimes**</span><span class="sxs-lookup"><span data-stu-id="54c55-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54c55-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="54c55-145">Gibt an, wie oft der Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54c55-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-146">**Auftragsstatus**</span><span class="sxs-lookup"><span data-stu-id="54c55-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54c55-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-149">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)".**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="54c55-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-150">Eine frei Form Zeichenfolge, die den Status des Auftrags darstellt.</span><span class="sxs-lookup"><span data-stu-id="54c55-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-151">**Localorutctime**</span><span class="sxs-lookup"><span data-stu-id="54c55-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-152">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54c55-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="54c55-154">Gibt an, ob die Uhrzeiten in den Eigenschaften **runstartinterval** und **UntilTime** Ortszeit oder UTC-Zeiten darstellen.</span><span class="sxs-lookup"><span data-stu-id="54c55-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="54c55-155">**Ortszeit** (1)</span><span class="sxs-lookup"><span data-stu-id="54c55-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="54c55-156">**UTC-Zeit** (2)</span><span class="sxs-lookup"><span data-stu-id="54c55-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54c55-157">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="54c55-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54c55-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="54c55-160">Der Benutzer, der benachrichtigt werden soll, wenn ein Auftrag abgeschlossen oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="54c55-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-161">**Otherherstellyaction**</span><span class="sxs-lookup"><span data-stu-id="54c55-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54c55-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-164">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Wiederherstellbares Action**")</span><span class="sxs-lookup"><span data-stu-id="54c55-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-165">Eine Zeichenfolge, die die Wiederherstellungs Aktion beschreibt, wenn die **Wiederherstellungs Action** -Eigenschaft " **other** " ("1") ist.</span><span class="sxs-lookup"><span data-stu-id="54c55-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="54c55-166">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="54c55-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54c55-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-169">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ owningjobelements**](cim-owningjobelement.md)")</span><span class="sxs-lookup"><span data-stu-id="54c55-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-170">Der Benutzer, der den Auftrag übermittelt hat, oder der Dienst-oder Methodenname, der den Auftrag angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="54c55-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="54c55-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54c55-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-174">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **Punit** ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="54c55-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-175">Der Prozentsatz des Auftrags, der beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="54c55-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="54c55-176">Der Wert "101" ist nicht definiert und wird in der nächsten Haupt Revision der Spezifikation nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="54c55-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="54c55-177">**Priority**</span><span class="sxs-lookup"><span data-stu-id="54c55-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-178">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54c55-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="54c55-180">Die Wichtigkeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="54c55-180">The importance of the job.</span></span> <span data-ttu-id="54c55-181">Je niedriger die Zahl, desto höher die Priorität.</span><span class="sxs-lookup"><span data-stu-id="54c55-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-182">**Wiederherstellbarkeits Aktion**</span><span class="sxs-lookup"><span data-stu-id="54c55-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54c55-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54c55-185">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Otherherstellyaction**")</span><span class="sxs-lookup"><span data-stu-id="54c55-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-186">Beschreibt die Wiederherstellungs Aktion, die ausgeführt werden soll, wenn ein laufauftrag fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="54c55-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54c55-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="54c55-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="54c55-188">Es ist unbekannt, welche Wiederherstellungs Aktion durchführen werden soll.</span><span class="sxs-lookup"><span data-stu-id="54c55-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="54c55-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="54c55-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="54c55-190">Die Wiederherstellungs Aktion wird in der **otherwiederherstellungsaction** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="54c55-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="54c55-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortsetzen** (2)</span><span class="sxs-lookup"><span data-stu-id="54c55-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="54c55-192">Beendet die Ausführung des Auftrags und aktualisiert seinen Status entsprechend.</span><span class="sxs-lookup"><span data-stu-id="54c55-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="54c55-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Fortfahren mit dem nächsten Auftrag** (3)</span><span class="sxs-lookup"><span data-stu-id="54c55-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="54c55-194">Fahren Sie mit dem nächsten Auftrag in der Warteschlange fort.</span><span class="sxs-lookup"><span data-stu-id="54c55-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="54c55-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)</span><span class="sxs-lookup"><span data-stu-id="54c55-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="54c55-196">Der Auftrag sollte erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="54c55-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="54c55-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Wiederherstellungsauftrag ausführen** (5)</span><span class="sxs-lookup"><span data-stu-id="54c55-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="54c55-198">Führen Sie den mit der **wiederherstellungsjob** -Beziehung verknüpften Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="54c55-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="54c55-199">Beachten Sie, dass sich der Wiederherstellungsauftrag bereits in der Warteschlange befinden muss, von der er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="54c55-200">**Runday**</span><span class="sxs-lookup"><span data-stu-id="54c55-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-201">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="54c55-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54c55-203">Qualifizierer: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Job**.**Runmonth**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")</span><span class="sxs-lookup"><span data-stu-id="54c55-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-204">Eine ganze Zahl, die in Verbindung mit der **rundayofweek** -Eigenschaft verwendet wird, um den Tag anzugeben, an dem der Auftrag verarbeitet wird. Wenn **rundayofweek** auf NULL festgelegt ist, gibt **runday** den Tag des Monats an, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="54c55-205">Wenn **runday** eine negative Ganzzahl ist, gibt Sie einen Tag relativ zum Ende des Monats an, oder wenn **runday** eine positive ganze Zahl ist, gibt Sie einen Tag relativ zum Anfang des Monats an.</span><span class="sxs-lookup"><span data-stu-id="54c55-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-206">**Rundayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="54c55-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-207">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="54c55-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54c55-209">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Runmonth**","**CIM- \_ Auftrag**.**Runday**","**CIM- \_ Auftrag**.**Runstartinterval**")</span><span class="sxs-lookup"><span data-stu-id="54c55-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-210">Eine ganze Zahl, die in Verbindung mit der **runday** -Eigenschaft verwendet wird, um den Tag anzugeben, an dem der Auftrag verarbeitet wird. Wenn **rundayofweek** auf NULL festgelegt ist, gibt **runday** den Tag des Monats an, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="54c55-211">**-Samstag** (-7)</span><span class="sxs-lookup"><span data-stu-id="54c55-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="54c55-212">**-Freitag** (-6)</span><span class="sxs-lookup"><span data-stu-id="54c55-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="54c55-213">**-Donnerstag** (-5)</span><span class="sxs-lookup"><span data-stu-id="54c55-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="54c55-214">**-Mittwoch** (-4)</span><span class="sxs-lookup"><span data-stu-id="54c55-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="54c55-215">**-Dienstag** (-3)</span><span class="sxs-lookup"><span data-stu-id="54c55-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="54c55-216">**-Montag** (-2)</span><span class="sxs-lookup"><span data-stu-id="54c55-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="54c55-217">**-Sonntag** (-1)</span><span class="sxs-lookup"><span data-stu-id="54c55-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="54c55-218">**Exactdayosmonth** (0)</span><span class="sxs-lookup"><span data-stu-id="54c55-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="54c55-219">**Sonntag** (1)</span><span class="sxs-lookup"><span data-stu-id="54c55-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="54c55-220">**Montag** (2)</span><span class="sxs-lookup"><span data-stu-id="54c55-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="54c55-221">**Dienstag** (3)</span><span class="sxs-lookup"><span data-stu-id="54c55-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="54c55-222">**Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="54c55-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="54c55-223">**Donnerstag** (5)</span><span class="sxs-lookup"><span data-stu-id="54c55-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="54c55-224">**Freitag** (6)</span><span class="sxs-lookup"><span data-stu-id="54c55-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="54c55-225">**Samstag** (7)</span><span class="sxs-lookup"><span data-stu-id="54c55-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54c55-226">**Runmonth**</span><span class="sxs-lookup"><span data-stu-id="54c55-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-227">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="54c55-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-228">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54c55-229">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Runday**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")</span><span class="sxs-lookup"><span data-stu-id="54c55-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-230">Der Monat, an dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="54c55-231">**Januar** (0)</span><span class="sxs-lookup"><span data-stu-id="54c55-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="54c55-232">**Februar** (1)</span><span class="sxs-lookup"><span data-stu-id="54c55-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="54c55-233">**März** (2)</span><span class="sxs-lookup"><span data-stu-id="54c55-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="54c55-234">**April** (3)</span><span class="sxs-lookup"><span data-stu-id="54c55-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="54c55-235">**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="54c55-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="54c55-236">**Juni** (5)</span><span class="sxs-lookup"><span data-stu-id="54c55-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="54c55-237">**Juli** (6)</span><span class="sxs-lookup"><span data-stu-id="54c55-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="54c55-238">**August** (7)</span><span class="sxs-lookup"><span data-stu-id="54c55-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="54c55-239">**September** (8)</span><span class="sxs-lookup"><span data-stu-id="54c55-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="54c55-240">**Oktober** (9)</span><span class="sxs-lookup"><span data-stu-id="54c55-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="54c55-241">**November** (10)</span><span class="sxs-lookup"><span data-stu-id="54c55-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="54c55-242">**Dezember** (11)</span><span class="sxs-lookup"><span data-stu-id="54c55-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54c55-243">**Runstartinterval**</span><span class="sxs-lookup"><span data-stu-id="54c55-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-244">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-245">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54c55-246">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Runmonth**","**CIM- \_ Auftrag**.**Runday**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")</span><span class="sxs-lookup"><span data-stu-id="54c55-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-247">Das Zeitintervall nach Mitternacht, zu dem der Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="54c55-248">"00000000020000.000000:000" gibt z. b. an, dass der Auftrag unter oder nach zwei Uhr Ortszeit oder UTC-Zeit (UTC mit der **localorutctime** -Eigenschaft angegeben) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="54c55-249">**Scheduledstarttime**</span><span class="sxs-lookup"><span data-stu-id="54c55-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-250">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-251">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54c55-252">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM- \_ Auftrag**.**Runmonth**","**CIM- \_ Auftrag**.**Runday**","**CIM- \_ Auftrag**.**Rundayof Week**","**CIM- \_ Auftrag**.**Runstartinterval**")</span><span class="sxs-lookup"><span data-stu-id="54c55-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="54c55-253">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="54c55-253">This property is deprecated.</span></span> <span data-ttu-id="54c55-254">Stattdessen empfiehlt es sich, die Eigenschaften **runmonth**, **runday**, **rundayosweek** und **runstartinterval** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="54c55-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="54c55-255">Der Zeitpunkt, zu dem der Start des aktuellen Auftrags geplant ist.</span><span class="sxs-lookup"><span data-stu-id="54c55-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="54c55-256">Diese Zeit kann durch ein Datum und eine Uhrzeit oder ein Intervall in Relation zum Zeitpunkt, zu dem die Eigenschaft angefordert wird, dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54c55-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="54c55-257">Ein Wert aller Nullen gibt an, dass der Auftrag bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-259">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c55-261">Der Zeitpunkt, zu dem der Auftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="54c55-261">The time when the job started.</span></span> <span data-ttu-id="54c55-262">Diese Zeit kann durch ein Datum und eine Uhrzeit oder durch ein Intervall dargestellt werden, das relativ zu dem Zeitpunkt ist, zu dem die Eigenschaft angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="54c55-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-263">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="54c55-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-264">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54c55-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c55-266">Der Zeitpunkt, zu dem der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="54c55-266">The time when the job was submitted.</span></span> <span data-ttu-id="54c55-267">Ein Wert aller Nullen gibt an, dass das übergeordnete Element kein Datum und keine Uhrzeit melden kann.</span><span class="sxs-lookup"><span data-stu-id="54c55-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="54c55-268">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c55-269">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="54c55-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54c55-270">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54c55-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54c55-271">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Auftrag**".**Localorutctime**")</span><span class="sxs-lookup"><span data-stu-id="54c55-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="54c55-272">Die Zeit, nach der der Auftrag ungültig wird oder angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="54c55-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="54c55-273">Die Zeit kann durch ein Datum und eine Uhrzeit oder durch ein Intervall in Relation zum Zeitpunkt, zu dem diese Eigenschaft angefordert wird, dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54c55-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="54c55-274">Ein Wert aller Neunen gibt an, dass der Auftrag unbegrenzt ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="54c55-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54c55-275">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54c55-275">Requirements</span></span>



| <span data-ttu-id="54c55-276">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54c55-276">Requirement</span></span> | <span data-ttu-id="54c55-277">Wert</span><span class="sxs-lookup"><span data-stu-id="54c55-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54c55-278">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54c55-278">Minimum supported client</span></span><br/> | <span data-ttu-id="54c55-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="54c55-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="54c55-280">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54c55-280">Minimum supported server</span></span><br/> | <span data-ttu-id="54c55-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54c55-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="54c55-282">Namespace</span><span class="sxs-lookup"><span data-stu-id="54c55-282">Namespace</span></span><br/>                | <span data-ttu-id="54c55-283">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="54c55-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54c55-284">MOF</span><span class="sxs-lookup"><span data-stu-id="54c55-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54c55-285"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54c55-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54c55-286">DLL</span><span class="sxs-lookup"><span data-stu-id="54c55-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54c55-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54c55-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54c55-288">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54c55-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c55-289">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="54c55-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

