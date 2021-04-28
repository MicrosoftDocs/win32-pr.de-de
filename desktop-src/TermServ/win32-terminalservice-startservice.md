---
title: StartService-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: 'StartService-Methode der Win32_Service-Klasse (Remotedesktopdienste): Versucht, den Dienst, auf den verwiesen wird, in seinen Startzustand zu platzieren.'
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- StartService-Methode Remotedesktopdienste
- StartService-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste , StartService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4bd12150223d7cdc1340b7557ba309a1e07da4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084198"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="4e377-106">StartService-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="4e377-106">StartService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="4e377-107">Die **StartService-Methode** versucht, den Dienst, auf den verwiesen wird, in seinen Startzustand zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="4e377-107">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="4e377-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e377-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e377-109">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="4e377-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e377-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e377-110">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="4e377-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e377-111">Parameters</span></span>

<span data-ttu-id="4e377-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4e377-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e377-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e377-113">Return value</span></span>

<span data-ttu-id="4e377-114">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4e377-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="4e377-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="4e377-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4e377-116">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="4e377-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4e377-117">**0**</span><span class="sxs-lookup"><span data-stu-id="4e377-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-118">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4e377-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-119">**1**</span><span class="sxs-lookup"><span data-stu-id="4e377-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-120">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e377-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-121">**2**</span><span class="sxs-lookup"><span data-stu-id="4e377-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-122">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="4e377-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-123">**3**</span><span class="sxs-lookup"><span data-stu-id="4e377-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-124">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="4e377-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-125">**4**</span><span class="sxs-lookup"><span data-stu-id="4e377-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="4e377-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-127">**5**</span><span class="sxs-lookup"><span data-stu-id="4e377-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-128">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)) ist.**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="4e377-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-129">**6**</span><span class="sxs-lookup"><span data-stu-id="4e377-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-130">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="4e377-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-131">**7**</span><span class="sxs-lookup"><span data-stu-id="4e377-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-132">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="4e377-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-133">**8**</span><span class="sxs-lookup"><span data-stu-id="4e377-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-134">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="4e377-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-135">**9**</span><span class="sxs-lookup"><span data-stu-id="4e377-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-136">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="4e377-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-137">**10**</span><span class="sxs-lookup"><span data-stu-id="4e377-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e377-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-139">**11**</span><span class="sxs-lookup"><span data-stu-id="4e377-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="4e377-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-141">**12**</span><span class="sxs-lookup"><span data-stu-id="4e377-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-142">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="4e377-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-143">**13**</span><span class="sxs-lookup"><span data-stu-id="4e377-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e377-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-145">**14**</span><span class="sxs-lookup"><span data-stu-id="4e377-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e377-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-147">**15**</span><span class="sxs-lookup"><span data-stu-id="4e377-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="4e377-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-149">**16**</span><span class="sxs-lookup"><span data-stu-id="4e377-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="4e377-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-151">**17**</span><span class="sxs-lookup"><span data-stu-id="4e377-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-152">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="4e377-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-153">**18**</span><span class="sxs-lookup"><span data-stu-id="4e377-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-154">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="4e377-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-155">**19**</span><span class="sxs-lookup"><span data-stu-id="4e377-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-156">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e377-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-157">**20**</span><span class="sxs-lookup"><span data-stu-id="4e377-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-158">Der Dienstname weist ungültige Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="4e377-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-159">**21**</span><span class="sxs-lookup"><span data-stu-id="4e377-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-160">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="4e377-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-161">**22**</span><span class="sxs-lookup"><span data-stu-id="4e377-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-162">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="4e377-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-163">**23**</span><span class="sxs-lookup"><span data-stu-id="4e377-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-164">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4e377-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e377-165">**24**</span><span class="sxs-lookup"><span data-stu-id="4e377-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="4e377-166">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="4e377-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e377-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e377-167">Remarks</span></span>

<span data-ttu-id="4e377-168">Es scheint zwar keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst zu geben, aber die beiden Zustände unterscheiden sich vom SCM.</span><span class="sxs-lookup"><span data-stu-id="4e377-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="4e377-169">Ein beendeter Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienststartprozedur durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="4e377-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="4e377-170">Ein angehaltener Dienst wird jedoch weiterhin ausgeführt, aber seine Funktion wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="4e377-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="4e377-171">Aus diesem Grund muss ein angehaltener Dienst nicht die gesamte Dienststartprozedur durchlaufen, sondern benötigt eine andere Prozedur, um die Funktionsweise fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4e377-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="4e377-172">Sie müssen die richtige Methode verwenden, um einen angehaltenen Dienst zu starten oder einen angehaltenen Dienst fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4e377-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="4e377-173">Die [**Win32-Dienstmethoden \_**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** und [**ResumeService**](win32-terminalservice-resumeservice.md) sollten in den folgenden Situationen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="4e377-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods **StartService** and [**ResumeService**](win32-terminalservice-resumeservice.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="4e377-174">Wenn ein Dienst derzeit beendet wird, müssen Sie ihn mithilfe der **StartService-Methode** neu starten. [**ResumeService**](win32-terminalservice-resumeservice.md) kann einen Dienst, der derzeit beendet ist, nicht starten.</span><span class="sxs-lookup"><span data-stu-id="4e377-174">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](win32-terminalservice-resumeservice.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="4e377-175">Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](win32-terminalservice-resumeservice.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e377-175">If a service is paused, you must use [**ResumeService**](win32-terminalservice-resumeservice.md).</span></span> <span data-ttu-id="4e377-176">Wenn Sie die **StartService-Methode** für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "Der Dienst wird bereits ausgeführt."</span><span class="sxs-lookup"><span data-stu-id="4e377-176">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="4e377-177">Der Dienst bleibt jedoch angehalten, bis der Dienststeuerungscode zum Fortsetzen an ihn gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e377-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="4e377-178">Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängig ist, werden beide Dienste gestartet.</span><span class="sxs-lookup"><span data-stu-id="4e377-178">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="4e377-179">Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="4e377-179">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="4e377-180">Sie müssen die Zuordnungsklasse [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) und die [Associators Of-Abfrage](/windows/desktop/WmiSdk/associators-of-statement) verwenden, um die Abhängigen zu suchen und separat zu starten.</span><span class="sxs-lookup"><span data-stu-id="4e377-180">You must use the association class [**Win32\_DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e377-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e377-181">Requirements</span></span>



| <span data-ttu-id="4e377-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e377-182">Requirement</span></span> | <span data-ttu-id="4e377-183">Wert</span><span class="sxs-lookup"><span data-stu-id="4e377-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e377-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e377-184">Minimum supported client</span></span><br/> | <span data-ttu-id="4e377-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e377-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e377-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e377-186">Minimum supported server</span></span><br/> | <span data-ttu-id="4e377-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e377-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e377-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e377-188">Namespace</span></span><br/>                | <span data-ttu-id="4e377-189">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4e377-189">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4e377-190">MOF</span><span class="sxs-lookup"><span data-stu-id="4e377-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e377-191"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e377-191"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e377-192">DLL</span><span class="sxs-lookup"><span data-stu-id="4e377-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e377-193"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e377-193"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e377-194">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e377-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e377-195">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="4e377-195">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="4e377-196">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="4e377-196">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="4e377-197">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="4e377-197">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="4e377-198">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="4e377-198">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

