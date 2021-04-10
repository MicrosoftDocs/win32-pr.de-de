---
description: Stellt einen Auftrag dar, der mit dem AT-Befehl erstellt wurde.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041361"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="ede6c-103">Win32 \_ ScheduledJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="ede6c-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="ede6c-104">Die **Win32 \_ ScheduledJob**- [WMI-Klasse](../wmisdk/retrieving-a-class.md)   stellt einen Auftrag dar, der mit dem **at** -Befehl erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ede6c-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="ede6c-105">Die **Win32 \_ ScheduledJob** -Klasse stellt keinen Auftrag dar, der mit dem Assistenten für geplante Aufgaben in der Systemsteuerung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ede6c-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="ede6c-106">Sie können eine von WMI erstellte Aufgabe nicht in der Benutzeroberfläche für geplante Aufgaben ändern.</span><span class="sxs-lookup"><span data-stu-id="ede6c-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="ede6c-107">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ede6c-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="ede6c-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ede6c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ede6c-109">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ede6c-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede6c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ede6c-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="ede6c-111">Member</span><span class="sxs-lookup"><span data-stu-id="ede6c-111">Members</span></span>

<span data-ttu-id="ede6c-112">Die **Win32 \_ ScheduledJob** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ede6c-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="ede6c-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="ede6c-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ede6c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ede6c-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ede6c-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="ede6c-115">Methods</span></span>

<span data-ttu-id="ede6c-116">Die **Win32 \_ ScheduledJob** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="ede6c-117">Methode</span><span class="sxs-lookup"><span data-stu-id="ede6c-117">Method</span></span>                                                      | <span data-ttu-id="ede6c-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ede6c-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ede6c-119">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="ede6c-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="ede6c-120">Klassenmethode, die einen Auftrag an das Betriebssystem übermittelt, um die Ausführung zu einem bestimmten Zeitpunkt (Datum und Uhrzeit) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ede6c-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="ede6c-121">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="ede6c-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="ede6c-122">Klassenmethode, die einen geplanten Auftrag löscht.</span><span class="sxs-lookup"><span data-stu-id="ede6c-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="ede6c-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ede6c-123">Properties</span></span>

<span data-ttu-id="ede6c-124">Die **Win32 \_ ScheduledJob** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ede6c-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ede6c-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ede6c-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-128">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ede6c-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-129">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ede6c-129">A short textual description of the object.</span></span>

<span data-ttu-id="ede6c-130">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-131">**Befehl**</span><span class="sxs-lookup"><span data-stu-id="ede6c-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-134">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-135">Der Name des Befehls, des Batch Programms oder der Binärdatei (und Befehlszeilenargumente), den der Zeit Plan Dienst zum Aufrufen des Auftrags verwendet.</span><span class="sxs-lookup"><span data-stu-id="ede6c-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="ede6c-136">Beispiel **: "Debug** - **/q/f**"</span><span class="sxs-lookup"><span data-stu-id="ede6c-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="ede6c-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ede6c-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-140">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_**](/windows/win32/api/lmat/ns-lmat-at_info) \| **infodaymonth**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-141">Tage des Monats, an denen die Ausführung des Auftrags geplant ist.</span><span class="sxs-lookup"><span data-stu-id="ede6c-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="ede6c-142">Wenn ein Auftrag für die Ausführung an mehreren Tagen des Monats geplant ist, können diese Werte in einem logischen OR-Vorgang verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="ede6c-143">Wenn ein Auftrag beispielsweise am 1. und 16. eines jeden Monats ausgeführt werden soll, ist der Wert der **daysOfMonth** -Eigenschaft 1 oder 32768.</span><span class="sxs-lookup"><span data-stu-id="ede6c-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="ede6c-144"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="ede6c-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-145">1.</span><span class="sxs-lookup"><span data-stu-id="ede6c-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="ede6c-146"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="ede6c-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-147">2.</span><span class="sxs-lookup"><span data-stu-id="ede6c-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="ede6c-148"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="ede6c-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-149">dritte</span><span class="sxs-lookup"><span data-stu-id="ede6c-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="ede6c-150"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="ede6c-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-151">4.</span><span class="sxs-lookup"><span data-stu-id="ede6c-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="ede6c-152"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="ede6c-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-153">5.</span><span class="sxs-lookup"><span data-stu-id="ede6c-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="ede6c-154"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="ede6c-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-155">6.</span><span class="sxs-lookup"><span data-stu-id="ede6c-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="ede6c-156"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="ede6c-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-157">7.</span><span class="sxs-lookup"><span data-stu-id="ede6c-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="ede6c-158"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="ede6c-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-159">8.</span><span class="sxs-lookup"><span data-stu-id="ede6c-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="ede6c-160"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="ede6c-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-161">9.</span><span class="sxs-lookup"><span data-stu-id="ede6c-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="ede6c-162"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="ede6c-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-163">10.</span><span class="sxs-lookup"><span data-stu-id="ede6c-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="ede6c-164"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="ede6c-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-165">11th</span><span class="sxs-lookup"><span data-stu-id="ede6c-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="ede6c-166"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="ede6c-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-167">12th</span><span class="sxs-lookup"><span data-stu-id="ede6c-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="ede6c-168"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="ede6c-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-169">13th</span><span class="sxs-lookup"><span data-stu-id="ede6c-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="ede6c-170"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="ede6c-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-171">14.</span><span class="sxs-lookup"><span data-stu-id="ede6c-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="ede6c-172"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="ede6c-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-173">15.</span><span class="sxs-lookup"><span data-stu-id="ede6c-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="ede6c-174"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="ede6c-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-175">16.</span><span class="sxs-lookup"><span data-stu-id="ede6c-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="ede6c-176"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="ede6c-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-177">17.</span><span class="sxs-lookup"><span data-stu-id="ede6c-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="ede6c-178"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="ede6c-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-179">18.</span><span class="sxs-lookup"><span data-stu-id="ede6c-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="ede6c-180"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="ede6c-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-181">19.</span><span class="sxs-lookup"><span data-stu-id="ede6c-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="ede6c-182"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="ede6c-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-183">20.</span><span class="sxs-lookup"><span data-stu-id="ede6c-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="ede6c-184"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="ede6c-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-185">21st</span><span class="sxs-lookup"><span data-stu-id="ede6c-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="ede6c-186"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="ede6c-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-187">22nd</span><span class="sxs-lookup"><span data-stu-id="ede6c-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="ede6c-188"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="ede6c-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-189">23rd</span><span class="sxs-lookup"><span data-stu-id="ede6c-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="ede6c-190"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="ede6c-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-191">24.</span><span class="sxs-lookup"><span data-stu-id="ede6c-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="ede6c-192"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="ede6c-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-193">25.</span><span class="sxs-lookup"><span data-stu-id="ede6c-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="ede6c-194"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="ede6c-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-195">26.</span><span class="sxs-lookup"><span data-stu-id="ede6c-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="ede6c-196"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="ede6c-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-197">27.</span><span class="sxs-lookup"><span data-stu-id="ede6c-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="ede6c-198"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="ede6c-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-199">28.</span><span class="sxs-lookup"><span data-stu-id="ede6c-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="ede6c-200"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="ede6c-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-201">29.</span><span class="sxs-lookup"><span data-stu-id="ede6c-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="ede6c-202"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="ede6c-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-203">30.</span><span class="sxs-lookup"><span data-stu-id="ede6c-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="ede6c-204"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="ede6c-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="ede6c-205">31.</span><span class="sxs-lookup"><span data-stu-id="ede6c-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ede6c-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="ede6c-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ede6c-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-209">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-210">Tage der Woche, an denen die Ausführung eines Auftrags geplant ist.</span><span class="sxs-lookup"><span data-stu-id="ede6c-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="ede6c-211">Wenn ein Auftrag für die Ausführung an mehreren Wochentagen geplant ist, können die Werte in einem logischen OR verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="ede6c-212">Wenn beispielsweise geplant ist, dass ein Auftrag montags, mittwochs und freitags ausgeführt wird, beträgt der Wert der **DaysOfWeek** -Eigenschaft 1 oder 4 oder 16.</span><span class="sxs-lookup"><span data-stu-id="ede6c-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="ede6c-213">**Montag** (1)</span><span class="sxs-lookup"><span data-stu-id="ede6c-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="ede6c-214">**Dienstag** (2)</span><span class="sxs-lookup"><span data-stu-id="ede6c-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="ede6c-215">**Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="ede6c-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="ede6c-216">**Donnerstag** (8)</span><span class="sxs-lookup"><span data-stu-id="ede6c-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="ede6c-217">**Freitag** (16)</span><span class="sxs-lookup"><span data-stu-id="ede6c-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="ede6c-218">**Samstag** (32)</span><span class="sxs-lookup"><span data-stu-id="ede6c-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="ede6c-219">**Sonntag** (64)</span><span class="sxs-lookup"><span data-stu-id="ede6c-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ede6c-220">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ede6c-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-223">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ede6c-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-224">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ede6c-224">A textual description of the object.</span></span>

<span data-ttu-id="ede6c-225">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-226">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="ede6c-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-227">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-229">Zeitspanne, für die der Auftrag ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ede6c-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="ede6c-230">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ede6c-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-232">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-234">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="ede6c-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-235">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ede6c-235">Indicates when the object was installed.</span></span> <span data-ttu-id="ede6c-236">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ede6c-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ede6c-237">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-238">**InteractWithDesktop**</span><span class="sxs-lookup"><span data-stu-id="ede6c-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-239">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ede6c-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-241">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job \_ noninteractive**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-242">Der angegebene Auftrag ist interaktiv. Dies bedeutet, dass ein Benutzer während der Ausführung eine Eingabe an einen geplanten Auftrag übergeben kann.</span><span class="sxs-lookup"><span data-stu-id="ede6c-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="ede6c-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-244">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ede6c-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-246">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-247">Identifizieren der Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="ede6c-247">Identifying number of the job.</span></span> <span data-ttu-id="ede6c-248">Sie wird von Methoden als Handle für einen Auftrag verwendet, der auf diesem Computer geplant wird.</span><span class="sxs-lookup"><span data-stu-id="ede6c-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-249">**Auftragsstatus**</span><span class="sxs-lookup"><span data-stu-id="ede6c-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-252">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Jobstatus"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **Flags** \| **Job \_ exec \_ Error**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-253">Ausführungs Status bei der letzten Ausführung des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="ede6c-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="ede6c-254">**Erfolg** ("Erfolg")</span><span class="sxs-lookup"><span data-stu-id="ede6c-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="ede6c-255">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ede6c-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ede6c-256">**Name**</span><span class="sxs-lookup"><span data-stu-id="ede6c-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-259">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ede6c-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-260">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="ede6c-260">Label by which the object is known.</span></span> <span data-ttu-id="ede6c-261">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ede6c-262">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-263">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="ede6c-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-266">Der Benutzer wird nach Abschluss oder Fehler des Auftrags benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="ede6c-267">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-268">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="ede6c-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-271">Der Benutzer, der den Auftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="ede6c-271">User who submitted the job.</span></span>

<span data-ttu-id="ede6c-272">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-273">**Priority**</span><span class="sxs-lookup"><span data-stu-id="ede6c-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-274">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ede6c-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-276">Wichtigkeit der Ausführung eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="ede6c-276">Importance of a job's execution.</span></span>

<span data-ttu-id="ede6c-277">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-278">**Runwiederholtes ausführen**</span><span class="sxs-lookup"><span data-stu-id="ede6c-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-279">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ede6c-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-281">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures on \| [**\_ Info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job in \_ \_ regelmäßigen Abständen ausführen**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-282">Der geplante Auftrag wird an den Tagen, an denen der Auftrag geplant ist, wiederholt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="ede6c-283">Wenn der Wert **false** ist, wird der Auftrag einmal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-285">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-287">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("StartTime"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**in \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **jobtime**")</span><span class="sxs-lookup"><span data-stu-id="ede6c-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-288">Die UTC-Zeit zum Ausführen des Auftrags in der Form "YYYYMMDDHHMMSS. Mmmmmm (+-) OOO ", wobei" YYYYMMDD "durch" "ersetzt werden muss \* \* \* \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="ede6c-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="ede6c-289">Der Austausch ist erforderlich, da der Planungsdienst nur das einmalige Ausführen von Aufträgen oder das Ausführen an einem Tag des Monats oder der Woche zulässt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="ede6c-290">Ein Auftrag kann nicht an einem bestimmten Datum ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="ede6c-291">Der Abschnitt "(+-) OOO" des **StartTime** -Eigenschafts Werts ist die aktuelle Abweichung für die lokale Zeit Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="ede6c-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="ede6c-292">Die Verschiebung ist der Unterschied zwischen UTC-Zeit und Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="ede6c-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="ede6c-293">Multiplizieren Sie die Anzahl der Stunden, die Ihre Zeitzone vor oder hinter der Ortszeit (GMT) um 60 liegen soll, um die Verschiebung für Ihre Zeitzone zu berechnen (verwenden Sie eine positive Zahl für die Anzahl von Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn sich Ihre Zeitzone hinter GMT befindet).</span><span class="sxs-lookup"><span data-stu-id="ede6c-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="ede6c-294">Fügen Sie der Berechnung eine zusätzliche 60 hinzu, wenn die Zeitzone die Sommerzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="ede6c-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="ede6c-295">Die Pacific Standard Time-Zone beträgt z. b. acht Stunden hinter GMT. Daher entspricht der Bias dem Wert-420 (-8 \* 60 + 60), wenn die Sommerzeit verwendet wird, und-480 (-8 \* 60), wenn die Sommerzeit nicht in Gebrauch ist.</span><span class="sxs-lookup"><span data-stu-id="ede6c-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="ede6c-296">Sie können auch den Wert der Bias ermitteln, indem Sie die Eigenschaft "Bias" der [**Win32- \_ Zeit Zonen**](win32-timezone.md) Klasse Abfragen.</span><span class="sxs-lookup"><span data-stu-id="ede6c-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="ede6c-297">Beispiel: " \* \* \* \* \* \* \* \* 123000.000000-420" gibt 14,30 (2:30 Uhr) an. PST mit Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="ede6c-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-298">**Status**</span><span class="sxs-lookup"><span data-stu-id="ede6c-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ede6c-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-301">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ede6c-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-302">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="ede6c-303">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ede6c-304">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="ede6c-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ede6c-305">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="ede6c-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ede6c-306">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="ede6c-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ede6c-307">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ede6c-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ede6c-308">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ede6c-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ede6c-309">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ede6c-310">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ede6c-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ede6c-311">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ede6c-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ede6c-312">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ede6c-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ede6c-313">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ede6c-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ede6c-314">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ede6c-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ede6c-315">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ede6c-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ede6c-316">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ede6c-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ede6c-317">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="ede6c-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ede6c-318">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ede6c-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ede6c-319">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="ede6c-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ede6c-320">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="ede6c-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ede6c-321">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="ede6c-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ede6c-322">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="ede6c-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ede6c-323">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="ede6c-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-324">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-326">Zeitpunkt, zu dem der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="ede6c-326">Time that the job was submitted.</span></span>

<span data-ttu-id="ede6c-327">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6c-328">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ede6c-329">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ede6c-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ede6c-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ede6c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ede6c-331">Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="ede6c-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="ede6c-332">Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](cim-job.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ede6c-333">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ede6c-333">Remarks</span></span>

<span data-ttu-id="ede6c-334">Jeder Auftrag, der für den Zeit Plan Dienst geplant ist, wird permanent gespeichert (der Planer kann einen Auftrag nach einem Neustart starten) und wird zum angegebenen Zeitpunkt und Tag der Woche oder des Monats ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="ede6c-335">Wenn der Computer nicht aktiv ist oder der geplante Dienst nicht zum angegebenen Zeitpunkt ausgeführt wird, wird der angegebene Auftrag vom Zeit Plan Dienst am nächsten Tag zum angegebenen Zeitpunkt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ede6c-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="ede6c-336">Aufträge werden gemäß der koordinierten Weltzeit (UTC) mit dem Versatz Offset von Greenwich Mean Time (GMT) geplant. Dies bedeutet, dass ein Auftrag mit einer beliebigen Zeitzone angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ede6c-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="ede6c-337">Die **Win32 \_ ScheduledJob** -Klasse gibt bei der Enumeration eines Objekts die Ortszeit mit dem UTC-Offset zurück und konvertiert die lokale Zeit beim Erstellen neuer Aufträge.</span><span class="sxs-lookup"><span data-stu-id="ede6c-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="ede6c-338">Beispiel: ein Auftrag, der zum Ausführen auf einem Computer in Boston um 10:30 Uhr angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ede6c-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="ede6c-339">Die Ortszeit der PST-Zeit wird für die lokale Ausführung um 1:30 Uhr geplant.</span><span class="sxs-lookup"><span data-stu-id="ede6c-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="ede6c-340">Dienstag EST.</span><span class="sxs-lookup"><span data-stu-id="ede6c-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="ede6c-341">Ein Client muss berücksichtigen, ob die Sommerzeit auf dem lokalen Computer in Betrieb ist, und wenn dies der Fall ist, subtrahieren Sie einen Bias von 60 Minuten vom UTC-Offset.</span><span class="sxs-lookup"><span data-stu-id="ede6c-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="ede6c-342">Die **Win32 \_ ScheduledJob** -Klasse wird vom [**CIM- \_ Auftrag**](cim-job.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ede6c-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="ede6c-343">Sie müssen Mitglied der Gruppe "Administratoren" sein, um einen geplanten Auftrag mit dieser Klasse erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="ede6c-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="ede6c-344">Die **Win32 \_ ScheduledJob** -Klasse verwendet intern das at-Protokoll, das ab Windows 8 und Windows Server 2012 als veraltet markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ede6c-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="ede6c-345">Im ersten Schritt ist das at-Protokollstandard mäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ede6c-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="ede6c-346">Wenn das Protokoll deaktiviert ist, kann beispielsweise der Aufruf der [**Create**](create-method-in-class-win32-scheduledjob.md) -Methode für ein **Win32 \_ ScheduledJob** -Objekt mit dem Fehler 0x8 fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="ede6c-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="ede6c-347">Sie können das at-Protokoll wieder aktivieren, indem Sie den folgenden Registrierungs Eintrag hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ede6c-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="ede6c-348">Möglicherweise müssen Sie den Computer neu starten, damit die Einstellung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="ede6c-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="ede6c-349">Da **Win32 \_ ScheduledJob** auf der Win32-API [**netschedulejobgetinfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) basiert, können Sie diese Klasse nicht zusammen mit der Taskplaner verwenden.</span><span class="sxs-lookup"><span data-stu-id="ede6c-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="ede6c-350">Wenn Sie Taskplaner verwenden möchten, verwenden Sie die Taskplaner-API.</span><span class="sxs-lookup"><span data-stu-id="ede6c-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="ede6c-351">Weitere Informationen finden Sie in der [Taskplaner-Referenz](../taskschd/task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ede6c-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ede6c-352">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ede6c-352">Examples</span></span>

<span data-ttu-id="ede6c-353">Im folgenden VBScript-Codebeispiel wird Notepad.exe für die interaktive tägliche Durchführung von 1:25 Uhr auf der lokalen Computerzeit geplant.</span><span class="sxs-lookup"><span data-stu-id="ede6c-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="ede6c-354">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ede6c-354">Requirements</span></span>



| <span data-ttu-id="ede6c-355">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ede6c-355">Requirement</span></span> | <span data-ttu-id="ede6c-356">Wert</span><span class="sxs-lookup"><span data-stu-id="ede6c-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ede6c-357">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ede6c-357">Minimum supported client</span></span><br/> | <span data-ttu-id="ede6c-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ede6c-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ede6c-359">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ede6c-359">Minimum supported server</span></span><br/> | <span data-ttu-id="ede6c-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ede6c-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ede6c-361">Namespace</span><span class="sxs-lookup"><span data-stu-id="ede6c-361">Namespace</span></span><br/>                | <span data-ttu-id="ede6c-362">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ede6c-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ede6c-363">MOF</span><span class="sxs-lookup"><span data-stu-id="ede6c-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ede6c-364"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ede6c-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ede6c-365">DLL</span><span class="sxs-lookup"><span data-stu-id="ede6c-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede6c-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ede6c-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede6c-367">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ede6c-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede6c-368">**CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="ede6c-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="ede6c-369">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="ede6c-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ede6c-370">WMI-Tasks: geplante Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ede6c-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
