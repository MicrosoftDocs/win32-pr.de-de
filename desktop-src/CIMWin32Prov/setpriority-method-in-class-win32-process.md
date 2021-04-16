---
description: Die SetPriority-&\# 32; Die WMI-Klassenmethode versucht, die Ausführungs Priorität des Prozesses zu ändern.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: SetPriority-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524144"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="ad683-103">SetPriority-Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="ad683-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="ad683-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetPriority** versucht, die Ausführungs Priorität des Prozesses zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ad683-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="ad683-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad683-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ad683-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ad683-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad683-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad683-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="ad683-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad683-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad683-109">*Priorität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad683-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad683-110">Neue Prioritäts Klasse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="ad683-110">New priority class for the process.</span></span> <span data-ttu-id="ad683-111">Beachten Sie, dass sich diese Werte von denen unterscheiden, die in der **Priority** -Eigenschaft des [**Win32- \_ Prozesses**](win32-process.md)explizit angegeben sind</span><span class="sxs-lookup"><span data-stu-id="ad683-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="ad683-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>Im **Leerlauf** (64)</span><span class="sxs-lookup"><span data-stu-id="ad683-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="ad683-113">Wird für einen Prozess mit Threads angegeben, die nur ausgeführt werden, wenn sich das System im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="ad683-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="ad683-114">Die Threads des Prozesses werden von den Threads eines Prozesses, der in einer höheren Prioritäts Klasse ausgeführt wird, z. b. einem Bildschirmschoner, vorzeitig entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad683-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="ad683-115">Die Klasse mit der inaktiven Priorität wird von untergeordneten Prozessen geerbt.</span><span class="sxs-lookup"><span data-stu-id="ad683-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="ad683-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>Niedriger als **Normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="ad683-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="ad683-117">Gibt einen Prozess an, der über eine Priorität oberhalb der inaktiven Prioritäts **\_ \_ Klasse**, aber unterhalb der **normalen \_ Prioritäts \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="ad683-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="ad683-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="ad683-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ad683-119">Wird für einen Prozess ohne besondere Planungsanforderungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad683-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="ad683-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Höher als normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="ad683-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="ad683-121">Gibt einen Prozess mit Priorität oberhalb der **normalen \_ Prioritäts \_ Klasse** an, aber unterhalb der **\_ \_ Klasse mit hoher Priorität**.</span><span class="sxs-lookup"><span data-stu-id="ad683-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="ad683-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Hohe Priorität** (128)</span><span class="sxs-lookup"><span data-stu-id="ad683-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="ad683-123">Wird für einen Prozess angegeben, der zeitkritische Aufgaben ausführt, die sofort ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ad683-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="ad683-124">Die Threads des Prozesses haben Vorrang vor den Threads von Prozessen in den Prioritätsklassen mit normaler oder Leerlaufpriorität.</span><span class="sxs-lookup"><span data-stu-id="ad683-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="ad683-125">Ein Beispiel hierfür ist die Aufgabenliste, die beim Aufrufen durch den Benutzer schnell reagieren muss, unabhängig von der Last des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="ad683-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="ad683-126">Verwenden Sie extrem Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, da eine Klasse mit hoher Priorität fast alle verfügbaren CPU-Zeit verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ad683-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="ad683-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span><span class="sxs-lookup"><span data-stu-id="ad683-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="ad683-128">Wird für einen Prozess mit der höchsten möglichen Priorität angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad683-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="ad683-129">Die Threads des Prozesses haben Vorrang vor den Threads aller anderen Prozesse, einschließlich der Betriebssystem Prozesse, von denen wichtige Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad683-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="ad683-130">Beispielsweise kann ein echt Zeit Prozess, der für mehr als ein sehr kurzes Intervall ausgeführt wird, dazu führen, dass Datenträger Caches nicht geleert werden oder die Maus nicht reagiert.</span><span class="sxs-lookup"><span data-stu-id="ad683-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad683-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad683-131">Return value</span></span>

<span data-ttu-id="ad683-132">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad683-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="ad683-133">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ad683-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ad683-134">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ad683-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ad683-135">**Erfolgreicher Abschluss** (0)</span><span class="sxs-lookup"><span data-stu-id="ad683-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ad683-136">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="ad683-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ad683-137">**Unzureichende Berechtigungen** (3)</span><span class="sxs-lookup"><span data-stu-id="ad683-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ad683-138">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="ad683-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ad683-139">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="ad683-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ad683-140">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="ad683-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ad683-141">**Sonstige** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="ad683-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ad683-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad683-142">Remarks</span></span>

<span data-ttu-id="ad683-143">Um die Priorität auf "Realtime" festzulegen, muss der Aufrufer über die Berechtigung " **seinkreasebasepriorityprivilege** " (**SE \_ Inc \_ Base \_ priority \_**) verfügen.</span><span class="sxs-lookup"><span data-stu-id="ad683-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="ad683-144">Ohne diese Berechtigung kann die höchste Priorität auf "hohe Priorität" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ad683-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="ad683-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad683-145">Examples</span></span>

<span data-ttu-id="ad683-146">Das Beispiel [Ändern der Priorität eines laufenden Prozesses](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript ändert die Priorität einer laufenden Instanz von Notepad.exe von normal auf höher.</span><span class="sxs-lookup"><span data-stu-id="ad683-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad683-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad683-147">Requirements</span></span>



| <span data-ttu-id="ad683-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad683-148">Requirement</span></span> | <span data-ttu-id="ad683-149">Wert</span><span class="sxs-lookup"><span data-stu-id="ad683-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad683-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad683-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ad683-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad683-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad683-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad683-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ad683-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad683-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad683-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad683-154">Namespace</span></span><br/>                | <span data-ttu-id="ad683-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ad683-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad683-156">MOF</span><span class="sxs-lookup"><span data-stu-id="ad683-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad683-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad683-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad683-158">DLL</span><span class="sxs-lookup"><span data-stu-id="ad683-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad683-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad683-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad683-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad683-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad683-161">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad683-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ad683-162">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="ad683-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

