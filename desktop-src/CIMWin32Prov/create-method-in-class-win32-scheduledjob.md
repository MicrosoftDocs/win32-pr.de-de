---
description: Übermittelt einen Auftrag an ein Betriebssystem zur Ausführung zu einem bestimmten Zeitpunkt und zum angegebenen Zeitpunkt in der Zukunft.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Create-Methode der Win32_ScheduledJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342349"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="61534-103">Create-Methode der Win32 \_ ScheduledJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="61534-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="61534-104">Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode sendet einen Auftrag an ein Betriebssystem zur Ausführung zu einem bestimmten Zeitpunkt und Datum in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="61534-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="61534-105">Diese Methode erfordert, dass der Zeit Plan Dienst auf dem Computer gestartet wird, an den der Auftrag übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="61534-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="61534-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="61534-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61534-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="61534-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61534-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61534-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="61534-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61534-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61534-110">*Befehl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61534-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-111">Der Name des Befehls, des Batch Programms oder der Binärdatei und Befehlszeilenparameter, die vom Zeit Plan Dienst zum Aufrufen des Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61534-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="61534-112">Beispiel: "Debug/q/f".</span><span class="sxs-lookup"><span data-stu-id="61534-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="61534-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61534-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-114">Koordinierte Weltzeit (UTC) zum Ausführen eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="61534-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="61534-115">Das Formular muss wie folgt lauten: "YYYYMMDDHHMMSS. Mmmmmm (+-) OOO ", wobei" YYYYMMDD "durch" "ersetzt werden muss \* \* \* \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="61534-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="61534-116">Beispiel: " \* \* \* \* \* \* \* \* 143000.000000-420" gibt 14,30 (2:30 Uhr) an. PST mit Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="61534-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="61534-117">Der Abschnitt "(+-) OOO" des StartTime-Eigenschafts Werts ist die aktuelle Abweichung für die lokale Zeit Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="61534-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="61534-118">Die Verschiebung ist der Unterschied zwischen der UTC-Zeit und der Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="61534-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="61534-119">Multiplizieren Sie die Anzahl der Stunden, die Ihre Zeitzone vor oder hinter der Ortszeit (GMT) um 60 liegen soll, um die Verschiebung für Ihre Zeitzone zu berechnen (verwenden Sie eine positive Zahl für die Anzahl von Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn sich Ihre Zeitzone hinter GMT befindet).</span><span class="sxs-lookup"><span data-stu-id="61534-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="61534-120">Fügen Sie der Berechnung eine zusätzliche 60 hinzu, wenn die Zeitzone die Sommerzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="61534-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="61534-121">Die Pacific Standard Time-Zone beträgt z. b. acht Stunden hinter GMT. Daher entspricht der Bias dem Wert-420 (-8 \* 60 + 60), wenn die Sommerzeit verwendet wird, und-480 (-8 \* 60), wenn die Sommerzeit nicht in Gebrauch ist.</span><span class="sxs-lookup"><span data-stu-id="61534-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="61534-122">Sie können auch den Wert der Bias ermitteln, indem Sie die Eigenschaft "Bias" der [**Win32- \_ Zeit Zonen**](win32-timezone.md) Klasse Abfragen.</span><span class="sxs-lookup"><span data-stu-id="61534-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="61534-123">*Runwiederholtes* \[ Ausführen in, optional\]</span><span class="sxs-lookup"><span data-stu-id="61534-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-124">**True** gibt an, dass ein geplanter Auftrag an bestimmten Tagen wiederholt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61534-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="61534-125">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="61534-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="61534-126">*DaysOfWeek* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="61534-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-127">Tage der Woche, an denen die Ausführung eines Auftrags geplant ist. wird nur verwendet, wenn der Parameter *runwiederholter* den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="61534-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="61534-128">Um einen Auftrag für mehr als einen Tag der Woche zu planen, verknüpfen Sie die entsprechenden Werte in einem logischen OR-Operator.</span><span class="sxs-lookup"><span data-stu-id="61534-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="61534-129">Wenn Sie z. b. einen Auftrag für Dienstag und freitags planen möchten, ist der Wert von *DaysOfWeek* 2 oder 16.</span><span class="sxs-lookup"><span data-stu-id="61534-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="61534-130">**Montag** (1)</span><span class="sxs-lookup"><span data-stu-id="61534-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="61534-131">**Dienstag** (2)</span><span class="sxs-lookup"><span data-stu-id="61534-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="61534-132">**Mittwoch** (4)</span><span class="sxs-lookup"><span data-stu-id="61534-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="61534-133">**Donnerstag** (8)</span><span class="sxs-lookup"><span data-stu-id="61534-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="61534-134">**Freitag** (16)</span><span class="sxs-lookup"><span data-stu-id="61534-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="61534-135">**Samstag** (32)</span><span class="sxs-lookup"><span data-stu-id="61534-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="61534-136">**Sonntag** (64)</span><span class="sxs-lookup"><span data-stu-id="61534-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="61534-137">*DaysOfMonth* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="61534-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-138">Tage des Monats, an denen die Ausführung eines Auftrags geplant ist. wird nur verwendet, wenn der Parameter *runwiederholter* den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="61534-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="61534-139"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="61534-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="61534-140">Tag 1 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="61534-141"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="61534-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="61534-142">Tag 2 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="61534-143"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="61534-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="61534-144">Tag 3 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="61534-145"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="61534-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="61534-146">Tag 4 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="61534-147"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="61534-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="61534-148">Tag 5 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="61534-149"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="61534-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="61534-150">Tag 6 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="61534-151"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="61534-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="61534-152">Tag 7 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="61534-153"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="61534-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="61534-154">Tag 8 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="61534-155"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="61534-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="61534-156">Tag 9 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="61534-157"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="61534-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="61534-158">Tag 10 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="61534-159"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="61534-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="61534-160">Tag 11 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="61534-161"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="61534-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="61534-162">Tag 12 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="61534-163"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="61534-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="61534-164">Tag 13 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="61534-165"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="61534-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="61534-166">Tag 14 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="61534-167"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="61534-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="61534-168">Tag 15 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="61534-169"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="61534-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="61534-170">Tag 16 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="61534-171"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="61534-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="61534-172">Tag 17 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="61534-173"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="61534-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="61534-174">Tag 18 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="61534-175"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="61534-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="61534-176">Tag 19 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="61534-177"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="61534-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="61534-178">Tag 20 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="61534-179"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="61534-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="61534-180">Tag 21 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="61534-181"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="61534-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="61534-182">Tag 22 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="61534-183"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="61534-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="61534-184">Tag 23 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="61534-185"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="61534-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="61534-186">Tag 24 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="61534-187"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="61534-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="61534-188">Tag 25 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="61534-189"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="61534-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="61534-190">Tag 26 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="61534-191"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="61534-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="61534-192">Tag 27 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="61534-193"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="61534-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="61534-194">Tag 28 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="61534-195"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="61534-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="61534-196">Tag 29 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="61534-197"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="61534-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="61534-198">Tag 30 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="61534-199"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="61534-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="61534-200">Tag 31 eines Monats</span><span class="sxs-lookup"><span data-stu-id="61534-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="61534-201">*InteractWithDesktop* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="61534-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-202">Wenn der Wert **true** ist, sollte der angegebene Auftrag interaktiv sein, was bedeutet, dass ein Benutzer während der Ausführung des Auftrags Eingaben an einen geplanten Auftrag übergeben kann.</span><span class="sxs-lookup"><span data-stu-id="61534-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="61534-203">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="61534-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="61534-204">*JobID* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="61534-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61534-205">Bezeichnernummer eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="61534-205">Identifier number of a job.</span></span> <span data-ttu-id="61534-206">Dieser Parameter ist ein Handle für einen Auftrag, der auf einem Computer geplant wird.</span><span class="sxs-lookup"><span data-stu-id="61534-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61534-207">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61534-207">Return value</span></span>

<span data-ttu-id="61534-208">Gibt bei erfolgreicher Ausführung den Wert 0 (null) und eine andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="61534-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="61534-209">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="61534-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="61534-210">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="61534-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="61534-211">**Erfolgreicher Abschluss**</span><span class="sxs-lookup"><span data-stu-id="61534-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="61534-212">0</span><span class="sxs-lookup"><span data-stu-id="61534-212">0</span></span>

<span data-ttu-id="61534-213">Die Anforderung wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="61534-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="61534-214">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="61534-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="61534-215">1</span><span class="sxs-lookup"><span data-stu-id="61534-215">1</span></span>

<span data-ttu-id="61534-216">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61534-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="61534-217">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="61534-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="61534-218">2</span><span class="sxs-lookup"><span data-stu-id="61534-218">2</span></span>

<span data-ttu-id="61534-219">Der Benutzer verfügt nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="61534-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="61534-220">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="61534-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="61534-221">8</span><span class="sxs-lookup"><span data-stu-id="61534-221">8</span></span>

<span data-ttu-id="61534-222">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="61534-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="61534-223">**Der Pfad wurde nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="61534-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="61534-224">9</span><span class="sxs-lookup"><span data-stu-id="61534-224">9</span></span>

<span data-ttu-id="61534-225">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="61534-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="61534-226">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="61534-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="61534-227">21</span><span class="sxs-lookup"><span data-stu-id="61534-227">21</span></span>

<span data-ttu-id="61534-228">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="61534-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="61534-229">**Dienst wurde nicht gestartet.**</span><span class="sxs-lookup"><span data-stu-id="61534-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="61534-230">22</span><span class="sxs-lookup"><span data-stu-id="61534-230">22</span></span>

<span data-ttu-id="61534-231">Das Konto, unter dem dieser Dienst ausgeführt wird, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="61534-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="61534-232">**Andere**</span><span class="sxs-lookup"><span data-stu-id="61534-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="61534-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="61534-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61534-234">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61534-234">Remarks</span></span>

<span data-ttu-id="61534-235">Wenn der geplante Auftrag ein interaktives Programm (z. b. Notepad) startet, muss die **interactwithdeskto** -Eigenschaft auf **true** festgelegt werden, oder der Programm Bildschirm ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="61534-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="61534-236">Der Prozess wird weiterhin im **Task-Manager** angezeigt, auch wenn er nicht auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="61534-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="61534-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61534-237">Requirements</span></span>



| <span data-ttu-id="61534-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61534-238">Requirement</span></span> | <span data-ttu-id="61534-239">Wert</span><span class="sxs-lookup"><span data-stu-id="61534-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61534-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61534-240">Minimum supported client</span></span><br/> | <span data-ttu-id="61534-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61534-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61534-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61534-242">Minimum supported server</span></span><br/> | <span data-ttu-id="61534-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61534-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61534-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="61534-244">Namespace</span></span><br/>                | <span data-ttu-id="61534-245">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="61534-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61534-246">MOF</span><span class="sxs-lookup"><span data-stu-id="61534-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61534-247"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="61534-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61534-248">DLL</span><span class="sxs-lookup"><span data-stu-id="61534-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61534-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61534-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61534-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61534-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="61534-251">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61534-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="61534-252">**Win32 \_ ScheduledJob**</span><span class="sxs-lookup"><span data-stu-id="61534-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

