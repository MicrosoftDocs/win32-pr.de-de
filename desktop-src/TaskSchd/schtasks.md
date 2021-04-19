---
title: Schtasks.exe
description: Ermöglicht es einem Administrator, geplante Aufgaben auf einem lokalen Computer oder einem Remote Computer zu erstellen, zu löschen, abzufragen, zu ändern, auszuführen und zu beenden.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Taskplaner
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1c9ba2c13053a8c550128f5d66623b5eed3a9dec
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314633"
---
# <a name="schtasksexe"></a><span data-ttu-id="e9c2e-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="e9c2e-104">Schtasks.exe</span></span>

<span data-ttu-id="e9c2e-105">Ermöglicht es einem Administrator, geplante Aufgaben auf einem lokalen Computer oder einem Remote Computer zu erstellen, zu löschen, abzufragen, zu ändern, auszuführen und zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="e9c2e-106">Wenn Sie Schtasks.exe ohne Argumente ausführen, werden der Status und die nächste Laufzeit für jede registrierte Aufgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="e9c2e-107">Weitere Informationen zu Taskplaner finden Sie in der folgenden Einführung: [Taskplaner für Entwickler](task-scheduler-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="e9c2e-108">Erstellen einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e9c2e-108">Creating a Task</span></span>

<span data-ttu-id="e9c2e-109">Die folgende Syntax wird verwendet, um eine Aufgabe auf dem lokalen Computer oder dem Remote Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a><span data-ttu-id="e9c2e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c2e-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-112">Ein-Wert, der den Remote Computer für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e9c2e-113">Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-115">Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-117">Ein-Wert, der das Kennwort für einen angegebenen Benutzer Kontext angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="e9c2e-118">Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/Ru** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-120">Ein-Wert, der den Benutzer Kontext angibt, unter dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="e9c2e-121">Gültige Werte für das Systemkonto sind "", "NT Authority \\ System" oder "System".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="e9c2e-122">Bei Taskplaner 2,0-Tasks sind auch "NT Authority \\ LocalService" und "NT Authority \\ Network Service" gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP aus** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-124">Ein-Wert, der das Kennwort für den mit dem/ru-Parameter angegebenen Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="e9c2e-125">Um zur Eingabe des Kennworts aufzufordern, muss der Wert entweder " \* " oder kein Wert sein.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="e9c2e-126">Dieses Kennwort wird für das Systemkonto ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-126">This password is ignored for the system account.</span></span> <span data-ttu-id="e9c2e-127">Dieser Parameter muss entweder mit/ru oder mit dem/XML-Schalter kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** </span><span class="sxs-lookup"><span data-stu-id="e9c2e-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-129">Ein-Wert, der die Zeit Plan Häufigkeit angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="e9c2e-130">Gültige Werte sind: Minute, stündlich, täglich, wöchentlich, monatlich, einmal, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Monat** - **Modifizierer**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-132">Ein Wert, der den Zeit Plantyp verfeinert, um eine präzisere Steuerung der Zeit Plan Wiederholung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="e9c2e-133">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e9c2e-133">Valid values are:</span></span>

-   <span data-ttu-id="e9c2e-134">Minute: 1-1439 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="e9c2e-135">Stündlich: 1-23 Stunden.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="e9c2e-136">Täglich: 1-365 Tage.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="e9c2e-137">Wöchentlich: 1-52.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="e9c2e-138">Once: keine Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="e9c2e-139">OnStart: keine Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="e9c2e-140">Onlogon: keine Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="e9c2e-141">OnIdle: keine Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="e9c2e-142">Monatlich: 1-12 oder erster, zweiter, Dritter, Vierter, letzter und Nachname.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="e9c2e-143">OnEvent: XPath-Ereignis Abfrage Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **Tage**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-145">Ein-Wert, der den Wochentag angibt, an dem die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="e9c2e-146">Gültige Werte sind Mon, di, Wed, Do, Fri, Sat, Sun und für monatliche Zeitpläne 1-31 (Tage des Monats)</span><span class="sxs-lookup"><span data-stu-id="e9c2e-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="e9c2e-147">Das Platzhalter Zeichen ( \* ) gibt alle Tage an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **Monate**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-149">Ein-Wert, der Monate des Jahres angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-149">A value that specifies months of the year.</span></span> <span data-ttu-id="e9c2e-150">Der Standardwert ist der erste Tag des Monats.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="e9c2e-151">Gültige Werte sind: Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov und Dec.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="e9c2e-152">Das Platzhalter Zeichen ( \* ) gibt alle Monate an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **IdleTime**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-154">Ein-Wert, der den Zeitraum angibt, der vor dem Ausführen einer geplanten OnIdle-Aufgabe gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="e9c2e-155">Der gültige Bereich ist 1-999 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-157">Ein-Wert, der einen Namen angibt, der die geplante Aufgabe eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-159">Ein-Wert, der den Pfad und den Dateinamen der Aufgabe angibt, die zum geplanten Zeitpunkt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="e9c2e-160">Beispiel: C: \\ Windows \\ system32 \\calc.exe.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-162">Ein-Wert, der die Startzeit zum Ausführen der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="e9c2e-163">Das Zeitformat ist hh: mm (24-Stunden-Zeit).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e9c2e-164">14:30 gibt beispielsweise 2:30Uhr an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="e9c2e-165">Der Standardwert ist die aktuelle Uhrzeit, an der/St nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="e9c2e-166">Diese Option ist für das/SC Once-Argument erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** - **Intervall**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-168">Ein-Wert, der das Wiederholungsintervall in Minuten angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="e9c2e-169">Dies gilt nicht für die folgenden Zeit Plan Typen: Minute, stündlich, OnStart, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="e9c2e-170">Der gültige Bereich ist 1-599940 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="e9c2e-171">Wenn entweder der/et-Parameter oder der/du-Parameter angegeben wird, beträgt der Standardwert 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="e9c2e-172">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-174">Ein-Wert, der die Endzeit angibt, zu der die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="e9c2e-175">Das Zeitformat ist hh: mm (24-Stunden-Zeit).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e9c2e-176">14:50 gibt beispielsweise 2:50uhr an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="e9c2e-177">Dies gilt nicht für die folgenden Zeit Plan Typen: OnStart, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="e9c2e-178">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** - **Dauer**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-180">Ein-Wert, der die Dauer angibt, mit der der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="e9c2e-181">Das Zeitformat ist hh: mm (24-Stunden-Zeit).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e9c2e-182">14:50 gibt beispielsweise 2:50uhr an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="e9c2e-183">Dies gilt nicht für/et und für die folgenden Zeit Plan Typen: OnStart, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="e9c2e-184">Bei/v1-Aufgaben (Taskplaner 1,0-Tasks), wenn/RI angegeben wird, ist der Standardwert für die Dauer 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="e9c2e-185">**Windows XP:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-187">Ein-Wert, der die Aufgabe zum Endzeit-oder Dauer Zeitpunkt beendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="e9c2e-188">Dies gilt nicht für die folgenden Zeit Plan Typen: OnStart, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="e9c2e-189">Es muss entweder/et oder/du angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="e9c2e-190">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-192">Ein-Wert, der das erste Datum angibt, an dem die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="e9c2e-193">Das Format ist "mm/dd/yyyy".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="e9c2e-194">Dieser Wert wird standardmäßig auf das aktuelle Datum eingestellt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-194">This value defaults to the current date.</span></span> <span data-ttu-id="e9c2e-195">Dies gilt nicht für die folgenden Zeit Plan Typen: Once, OnStart, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-197">Ein-Wert, der das letzte Datum angibt, an dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="e9c2e-198">Das Format ist "mm/dd/yyyy".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="e9c2e-199">Dies gilt nicht für die folgenden Zeit Plan Typen: Once, OnStart, onlogon, OnIdle und OnEvent.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-201">Ein-Wert, der den Ereignis Kanal für OnEvent-Trigger angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="e9c2e-202">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-204">Ein Wert, mit dem die Aufgabe interaktiv ausgeführt werden kann, wenn der/ru-Benutzer zurzeit beim Ausführen der Aufgabe angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="e9c2e-205">Der Task wird nur ausgeführt, wenn der Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="e9c2e-206">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-208">Ein Wert, der angibt, dass kein Kennwort gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="e9c2e-209">Der Task wird nicht interaktiv als der angegebene Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="e9c2e-210">Es sind nur lokale Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-210">Only local resources are available.</span></span>

<span data-ttu-id="e9c2e-211">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-212"><span id="_Z_"></span><span id="_z_"></span>**"/Z**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-213">Ein-Wert, der die Aufgabe kennzeichnet, die nach der letzten Ausführung gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="e9c2e-214">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-216">Ein-Wert, der eine Aufgabe aus einer XML-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="e9c2e-217">Dieser Parameter kann mit/ru-und/RP aus-Switches oder mit dem/RP aus-Switch allein kombiniert werden, wenn die Task-XML bereits den Prinzipal enthält.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="e9c2e-218">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-220">Ein Wert, der eine Aufgabe erstellt, die für die Plattformen Windows 2000, Windows Server 2003 und Windows XP sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="e9c2e-221">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-223">Ein Wert, der die Aufgabe erzwungen erstellt und Warnungen unterdrückt, wenn die angegebene Aufgabe bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="e9c2e-224">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** - **Ebene**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-226">Ein-Wert, der die Ausführungs Ebene für die Aufgabe festlegt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="e9c2e-227">Gültige Werte sind Limited und höchste.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="e9c2e-228">Der Standardwert ist "Limited".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-228">The default is LIMITED.</span></span>

<span data-ttu-id="e9c2e-229">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delta Time**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-231">Ein-Wert, der die Wartezeit angibt, nach der der Task nach dem Auslösen des Auslösers verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="e9c2e-232">Das Zeitformat ist mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="e9c2e-233">Diese Option ist nur für die Zeit Plan Typen OnStart, onlogon und OnEvent gültig.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="e9c2e-234">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-236">Ein-Wert, der die Hilfe Meldung für Schtasks.exe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9c2e-237">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9c2e-237">Remarks</span></span>

<span data-ttu-id="e9c2e-238">Verwenden Sie beim Erstellen einer Aufgabe auf einem Remote Computer, auf dem das Betriebssystem Windows XP, Windows Server 2003 oder Windows 2000 ausgeführt wird, den/v1-Schalter.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="e9c2e-239">Sie können keine nicht interaktive Remote Taskplaner 1,0-Aufgabe erstellen (erstellen Sie einen Task, indem Sie den Schalter/IT nicht verwenden, und verwenden Sie den Schalter/v1), wenn auf dem Remote Computer die Firewallausnahme für Datei-und Druckerfreigabe aktiviert ist und die Firewallausnahme für die Remote Verwaltung geplanter Tasks deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="e9c2e-240">Löschen einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e9c2e-240">Deleting a Task</span></span>

<span data-ttu-id="e9c2e-241">Die folgende Syntax wird verwendet, um eine oder mehrere geplante Tasks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a><span data-ttu-id="e9c2e-242">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c2e-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c2e-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-244">Ein-Wert, der den Remote Computer für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e9c2e-245">Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-247">Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-249">Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e9c2e-250">Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-252">Ein-Wert, der den Namen der zu löschenden geplanten Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="e9c2e-253">Das Platzhalter Zeichen ( \* ) kann verwendet werden, um alle Aufgaben zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-255">Ein Wert, der die Aufgabe erzwungen und Warnungen unterdrückt, wenn die angegebene Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-257">Ein-Wert, der die Hilfe für Schtasks.exe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="e9c2e-258">Ausführen einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e9c2e-258">Running a Task</span></span>

<span data-ttu-id="e9c2e-259">Die folgende Syntax wird verwendet, um eine geplante Aufgabe sofort auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a><span data-ttu-id="e9c2e-260">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c2e-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c2e-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-262">Ein-Wert, der den Remote Computer für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e9c2e-263">Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-265">Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-267">Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e9c2e-268">Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-270">Ein-Wert, der den Namen des geplanten Tasks angibt, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-272">Ein-Wert, der die Hilfe für Schtasks.exe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="e9c2e-273">Beenden einer laufenden Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e9c2e-273">Ending a Running Task</span></span>

<span data-ttu-id="e9c2e-274">Die folgende Syntax wird verwendet, um eine laufende geplante Aufgabe zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="e9c2e-275">Um das Ausführen einer Remote Aufgabe zu verhindern, stellen Sie sicher, dass der Remote Computer über die Datei-und Druckerfreigabe und die Verwaltung von Firewallausnahmen für Remote geplante Tasks verfügt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a><span data-ttu-id="e9c2e-276">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c2e-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c2e-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-278">Ein-Wert, der den Remote Computer für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e9c2e-279">Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-281">Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-283">Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e9c2e-284">Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-286">Ein-Wert, der den Namen der geplanten Aufgabe angibt, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-288">Ein-Wert, der die Hilfe für Schtasks.exe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="e9c2e-289">Abfragen von Task Informationen</span><span class="sxs-lookup"><span data-stu-id="e9c2e-289">Querying for Task Information</span></span>

<span data-ttu-id="e9c2e-290">Die folgende Syntax wird verwendet, um die geplanten Tasks auf dem lokalen Computer oder dem Remote Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a><span data-ttu-id="e9c2e-291">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c2e-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c2e-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-293">Ein-Wert, der den Remote Computer für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e9c2e-294">Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-296">Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-298">Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e9c2e-299">Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** - **Format**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-301">Ein-Wert, der das Ausgabeformat angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-301">A value that specifies the output format.</span></span> <span data-ttu-id="e9c2e-302">Gültige Werte sind "Table", "List" und "CSV".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-304">Ein-Wert, der angibt, dass der Spaltenheader nicht in der Ausgabe angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="e9c2e-305">Dies gilt nur für Tabellen-und CSV-Formate.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-307">Ein-Wert, der ausführliche Task Ausgaben anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="e9c2e-308">Wenn für eine Aufgabe nur ein einziges Mal ausgeführt werden soll, sind die angezeigten Zeit Plan Informationen "Zeit Plan Daten sind in diesem Format nicht verfügbar".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="e9c2e-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-310">Ein-Wert, der den Aufgaben Namen angibt, für den die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="e9c2e-311">Wenn kein Aufgaben Name angegeben ist, werden Informationen zu allen Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="e9c2e-312">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-314">Ein-Wert, der verwendet wird, um die Aufgaben Definitionen im XML-Format anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="e9c2e-315">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-317">Ein-Wert, der verwendet wird, um die Hilfe für Schtasks.exe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="e9c2e-318">Ändern einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e9c2e-318">Changing a Task</span></span>

<span data-ttu-id="e9c2e-319">Die folgende Syntax wird verwendet, um die Ausführung des Programms zu ändern oder um das von einer geplanten Aufgabe verwendete Benutzerkonto und Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a><span data-ttu-id="e9c2e-320">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c2e-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c2e-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** - **System**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-322">Ein-Wert, der den Remote Computer für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e9c2e-323">Wenn kein Wert angegeben wird, wird der Systemparameter standardmäßig auf dem lokalen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-325">Ein-Wert, der den Benutzer Kontext angibt, unter dem Schtasks.exe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ Kennwort \]**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-327">Ein-Wert, der das Kennwort für den angegebenen Benutzer Kontext angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e9c2e-328">Wenn die Angabe ausgelassen wird, fordert Schtasks.exe den Benutzer zur Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Taskname**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-330">Ein-Wert, der angibt, welche geplante Aufgabe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-332">Ein-Wert, der den Benutzernamen (Benutzer Kontext) ändert, unter dem die geplante Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="e9c2e-333">Gültige Werte für das Systemkonto sind "", "NT Authority \\ System" oder "System".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="e9c2e-334">Bei Taskplaner 2,0-Tasks sind auch "NT Authority \\ LocalService" und "NT Authority \\ Network Service" gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP aus** **runaspassword**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-336">Ein-Wert, der ein neues Kennwort für den vorhandenen Benutzer Kontext oder das Kennwort für ein neues Benutzerkonto angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="e9c2e-337">Dieses Kennwort wird für das Systemkonto ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-339">Ein-Wert, der ein neues Programm angibt, das vom Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-341">Ein-Wert, der die Startzeit zum Ausführen der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="e9c2e-342">Das Zeitformat ist hh: mm (24-Stunden-Zeit).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e9c2e-343">14:30 gibt beispielsweise 2:30Uhr an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="e9c2e-344">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** - **Intervall**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-346">Ein-Wert, der das Wiederholungsintervall in Minuten angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="e9c2e-347">Der gültige Bereich ist 1-599940 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="e9c2e-348">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-350">Ein-Wert, der die Endzeit der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="e9c2e-351">Das Zeitformat ist hh: mm (24-Stunden-Zeit).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e9c2e-352">14:50 gibt beispielsweise 2:50uhr an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="e9c2e-353">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** - **Dauer**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-355">Ein-Wert, der die Dauer angibt, mit der der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="e9c2e-356">Das Zeitformat ist hh: mm (24-Stunden-Zeit).</span><span class="sxs-lookup"><span data-stu-id="e9c2e-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e9c2e-357">14:50 gibt beispielsweise 2:50uhr an.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="e9c2e-358">Dies gilt nicht für den/et-Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="e9c2e-359">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-361">Ein-Wert, der die Aufgabe zum Endzeit-oder Dauer Zeitpunkt beendet.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="e9c2e-362">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-364">Ein-Wert, der das erste Datum angibt, an dem die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="e9c2e-365">Das Format ist "mm/dd/yyyy".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="e9c2e-366">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-368">Ein-Wert, der das letzte Datum angibt, an dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="e9c2e-369">Das Format ist "mm/dd/yyyy".</span><span class="sxs-lookup"><span data-stu-id="e9c2e-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="e9c2e-370">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-372">Ein Wert, mit dem die Aufgabe interaktiv ausgeführt werden kann, wenn der/ru-Benutzer zurzeit beim Ausführen der Aufgabe angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="e9c2e-373">Der Task wird nur ausgeführt, wenn der Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="e9c2e-374">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** - **Ebene**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-376">Ein-Wert, der die Ausführungs Ebene für die Aufgabe festlegt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="e9c2e-377">Gültige Werte sind Limited und höchste.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="e9c2e-378">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-380">Ein-Wert, der die geplante Aufgabe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="e9c2e-381">Eine aktivierte Aufgabe kann ausgeführt werden, und eine deaktivierte Aufgabe kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="e9c2e-382">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/Disable**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-384">Ein-Wert, der die Ausführung der geplanten Aufgabe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="e9c2e-385">Wenn eine Remote Taskplaner 1,0-Aufgabe durch Schtasks.exe deaktiviert wird und auf dem Remote Computer die Firewallausnahme für Datei-und Druckerfreigabe aktiviert ist und die Firewallausnahme für die Remote Verwaltung geplanter Tasks deaktiviert ist, wird die Aufgabe beim Lesen aus einer Taskplaner 2,0-API nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="e9c2e-386">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-387"><span id="_Z_"></span><span id="_z_"></span>**"/Z**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-388">Ein-Wert, der die Aufgabe kennzeichnet, die nach der letzten Ausführung gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="e9c2e-389">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delta Time**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="e9c2e-391">Ein-Wert, der die Wartezeit angibt, nach der die Ausführung der Aufgabe nach dem Auslösen des Auslösers verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="e9c2e-392">Das Zeitformat ist mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="e9c2e-393">Diese Option ist nur für Tasks mit den Zeit Plan Typen OnStart, onlogon und OnEvent gültig.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="e9c2e-394">**Windows XP und Windows Server 2003:** Diese Option ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e9c2e-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e9c2e-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="e9c2e-396">Ein-Wert, der die Hilfe Meldung für Schtasks.exe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9c2e-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9c2e-397">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9c2e-397">Requirements</span></span>



| <span data-ttu-id="e9c2e-398">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9c2e-398">Requirement</span></span> | <span data-ttu-id="e9c2e-399">Wert</span><span class="sxs-lookup"><span data-stu-id="e9c2e-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9c2e-400">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9c2e-400">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c2e-401">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9c2e-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e9c2e-402">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9c2e-402">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c2e-403">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9c2e-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





