---
title: ResumeService-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Versucht, den Dienst, auf den verwiesen wird, im Zustand "fortgesetzt"
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- ResumeService-Methode Remotedesktopdienste
- ResumeService-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, ResumeService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7b446dea84e4320e9aa8972a88dc4fdd5a6eea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518821"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="77d68-106">ResumeService-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="77d68-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="77d68-107">Die **ResumeService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, den Dienst, auf den verwiesen wird, in den Status "fortgesetzt"</span><span class="sxs-lookup"><span data-stu-id="77d68-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="77d68-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="77d68-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="77d68-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="77d68-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="77d68-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="77d68-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="77d68-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="77d68-111">Parameters</span></span>

<span data-ttu-id="77d68-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="77d68-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77d68-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77d68-113">Return value</span></span>

<span data-ttu-id="77d68-114">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="77d68-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="77d68-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="77d68-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="77d68-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="77d68-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="77d68-117">**0**</span><span class="sxs-lookup"><span data-stu-id="77d68-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-118">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="77d68-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-119">**1**</span><span class="sxs-lookup"><span data-stu-id="77d68-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-120">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="77d68-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-121">**2**</span><span class="sxs-lookup"><span data-stu-id="77d68-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-122">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="77d68-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-123">**3**</span><span class="sxs-lookup"><span data-stu-id="77d68-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-124">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="77d68-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-125">**4**</span><span class="sxs-lookup"><span data-stu-id="77d68-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="77d68-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-127">**5**</span><span class="sxs-lookup"><span data-stu-id="77d68-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-128">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="77d68-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-129">**6**</span><span class="sxs-lookup"><span data-stu-id="77d68-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-130">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="77d68-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-131">**7**</span><span class="sxs-lookup"><span data-stu-id="77d68-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-132">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="77d68-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-133">**8**</span><span class="sxs-lookup"><span data-stu-id="77d68-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-134">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="77d68-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-135">**9**</span><span class="sxs-lookup"><span data-stu-id="77d68-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-136">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="77d68-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-137">**10**</span><span class="sxs-lookup"><span data-stu-id="77d68-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77d68-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-139">**11**</span><span class="sxs-lookup"><span data-stu-id="77d68-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="77d68-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-141">**12**</span><span class="sxs-lookup"><span data-stu-id="77d68-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-142">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="77d68-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-143">**13**</span><span class="sxs-lookup"><span data-stu-id="77d68-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="77d68-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-145">**14**</span><span class="sxs-lookup"><span data-stu-id="77d68-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="77d68-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-147">**15**</span><span class="sxs-lookup"><span data-stu-id="77d68-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="77d68-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-149">**16**</span><span class="sxs-lookup"><span data-stu-id="77d68-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="77d68-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-151">**17**</span><span class="sxs-lookup"><span data-stu-id="77d68-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-152">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="77d68-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-153">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="77d68-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-154">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="77d68-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-155">**19**</span><span class="sxs-lookup"><span data-stu-id="77d68-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-156">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77d68-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-157">**20**</span><span class="sxs-lookup"><span data-stu-id="77d68-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-158">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="77d68-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-159">**21**</span><span class="sxs-lookup"><span data-stu-id="77d68-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-160">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="77d68-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-161">**22**</span><span class="sxs-lookup"><span data-stu-id="77d68-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-162">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="77d68-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-163">**23**</span><span class="sxs-lookup"><span data-stu-id="77d68-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-164">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="77d68-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="77d68-165">**24**</span><span class="sxs-lookup"><span data-stu-id="77d68-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="77d68-166">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="77d68-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77d68-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77d68-167">Remarks</span></span>

<span data-ttu-id="77d68-168">Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst gibt, werden die beiden Zustände anders als der SCM angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77d68-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="77d68-169">Ein angehaltener Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienst Start Prozedur durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="77d68-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="77d68-170">Ein angehaltene Dienst wird jedoch weiterhin ausgeführt, aber seine funktionstüchtig ist angehalten.</span><span class="sxs-lookup"><span data-stu-id="77d68-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="77d68-171">Aus diesem Grund muss ein angehaltene Dienst nicht die gesamte Dienst Start Prozedur durchlaufen, sondern erfordert ein anderes Verfahren, um die Funktionsweise fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="77d68-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="77d68-172">Sie müssen die richtige-Methode verwenden, um einen Dienst zu starten, der angehalten wurde, oder um einen Dienst fortzusetzen, der angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="77d68-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="77d68-173">Die [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Methoden " [**StartService**](win32-terminalservice-startservice.md) " und " **ResumeService** " sollten in den folgenden Situationen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="77d68-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="77d68-174">Wenn ein Dienst aktuell beendet ist, müssen Sie ihn mit der [**Start Service**](win32-terminalservice-startservice.md) -Methode neu starten. **ResumeService** kann einen Dienst nicht starten, der zurzeit beendet ist.</span><span class="sxs-lookup"><span data-stu-id="77d68-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="77d68-175">Wenn ein Dienst angehalten wird, müssen Sie **ResumeService** verwenden.</span><span class="sxs-lookup"><span data-stu-id="77d68-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="77d68-176">Wenn Sie die [**Start Service**](win32-terminalservice-startservice.md) -Methode für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "der Dienst wird bereits ausgeführt."</span><span class="sxs-lookup"><span data-stu-id="77d68-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="77d68-177">Der Dienst bleibt jedoch angehalten, bis der Steuerungs Code zum Fortsetzen des dienstandens an ihn gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="77d68-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="77d68-178">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77d68-178">Examples</span></span>

<span data-ttu-id="77d68-179">Das Beispiel zum fort [setzen von Autostart-Diensten mit angehaltenen](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript startet alle automatischen Start Dienste neu, die angehalten wurden.</span><span class="sxs-lookup"><span data-stu-id="77d68-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d68-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77d68-180">Requirements</span></span>



| <span data-ttu-id="77d68-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77d68-181">Requirement</span></span> | <span data-ttu-id="77d68-182">Wert</span><span class="sxs-lookup"><span data-stu-id="77d68-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77d68-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77d68-183">Minimum supported client</span></span><br/> | <span data-ttu-id="77d68-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77d68-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77d68-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77d68-185">Minimum supported server</span></span><br/> | <span data-ttu-id="77d68-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77d68-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77d68-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="77d68-187">Namespace</span></span><br/>                | <span data-ttu-id="77d68-188">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="77d68-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="77d68-189">MOF</span><span class="sxs-lookup"><span data-stu-id="77d68-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77d68-190"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="77d68-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="77d68-191">DLL</span><span class="sxs-lookup"><span data-stu-id="77d68-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77d68-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77d68-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d68-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77d68-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d68-194">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="77d68-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="77d68-195">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="77d68-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="77d68-196">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="77d68-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="77d68-197">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="77d68-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

