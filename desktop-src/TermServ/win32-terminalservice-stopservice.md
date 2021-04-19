---
title: Stop Service-Methode der Win32_Service-Klasse ("sdoias. h") (Terminal Dienst)
description: Platziert den Dienst, der durch das Win32 \_ Terminalservice-Objekt dargestellt wird, im beendeten Zustand.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Stop Service-Methode Remotedesktopdienste
- Stop Service-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service Class Remotedesktopdienste, StopService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106372017"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="0d7e1-106">Stop Service-Methode der Win32_Service-Klasse (sdoias. h) für den Terminal Dienst</span><span class="sxs-lookup"><span data-stu-id="0d7e1-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="0d7e1-107">Die **StopService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versetzt den Dienst, der durch das [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Objekt dargestellt wird, in den Zustand "beendet".</span><span class="sxs-lookup"><span data-stu-id="0d7e1-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="0d7e1-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d7e1-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0d7e1-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d7e1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d7e1-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="0d7e1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d7e1-111">Parameters</span></span>

<span data-ttu-id="0d7e1-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d7e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d7e1-113">Return value</span></span>

<span data-ttu-id="0d7e1-114">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="0d7e1-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0d7e1-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0d7e1-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0d7e1-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0d7e1-117">**0**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-118">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-119">**1**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-120">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-121">**2**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-122">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-123">**3**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-124">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-125">**4**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-127">**5**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-128">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-129">**6**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-130">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-131">**7**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-132">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-133">**8**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-134">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-135">**9**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-136">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-137">**10**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-139">**11**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-141">**12**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-142">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-143">**13**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-145">**14**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-147">**15**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-149">**16**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-151">**17**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-152">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-153">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-154">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-155">**19**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-156">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-157">**20**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-158">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-159">**21**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-160">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-161">**22**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-162">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-163">**23**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-164">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d7e1-165">**24**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0d7e1-166">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d7e1-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d7e1-167">Remarks</span></span>

<span data-ttu-id="0d7e1-168">Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die-Methode **StopService** und die [**anhaleservice**](win32-terminalservice-pauseservice.md) -Methode verwenden, um-Dienste anzuhalten und anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="0d7e1-169">Die Entscheidung, einen Dienst zu stoppen, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="0d7e1-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="0d7e1-170">Ist der Dienst in der Lage, angehalten zu werden?</span><span class="sxs-lookup"><span data-stu-id="0d7e1-170">Is the service capable of being paused?</span></span> <span data-ttu-id="0d7e1-171">Wenn dies nicht der Wert ist, ist die einzige Option der Dienst wird beendet.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="0d7e1-172">Müssen Sie die Verarbeitung von Client Anforderungen für alle Benutzer fortsetzen, die bereits mit dem Dienst verbunden sind?</span><span class="sxs-lookup"><span data-stu-id="0d7e1-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="0d7e1-173">Wenn dies der Fall ist, ermöglicht das Anhalten eines Dienstanbieter in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert</span><span class="sxs-lookup"><span data-stu-id="0d7e1-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="0d7e1-174">Wenn Sie einen Dienst beenden, werden dagegen alle Clients sofort getrennt.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="0d7e1-175">Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden?</span><span class="sxs-lookup"><span data-stu-id="0d7e1-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="0d7e1-176">Obwohl Dienst Eigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten nicht wirksam, bis der Dienst tatsächlich beendet und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="0d7e1-177">Der zum Anhalten eines Dienstanbieter erforderliche Skriptcode ist nahezu identisch mit dem Code, der zum Anhalten des Dienstanbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="0d7e1-178">Wenn Sie versuchen, einen Dienst zu beenden, für den abhängige Dienste ausgeführt werden, schlägt die **Stop Service** -Methode mit einem Rückgabewert von 3 fehl.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="0d7e1-179">Die abhängigen Dienste müssen zuerst beendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="0d7e1-180">Wenn Sie einen Dienst beenden, überprüfen Sie den [**Win32 \_ Terminalservice**](win32-terminalservice.md)sofort.**State** -Eigenschaft, da der Dienst möglicherweise weiterhin als wird ausgeführt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="0d7e1-181">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d7e1-181">Examples</span></span>

<span data-ttu-id="0d7e1-182">[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell-Beispiel legt den Dienststatus für Remote Computer fest.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="0d7e1-183">Das Beispiel zum [Beenden eines Diensts und seiner abhängigen](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript beendet einen Dienst und alle abhängigen Dienste.</span><span class="sxs-lookup"><span data-stu-id="0d7e1-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d7e1-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d7e1-184">Requirements</span></span>



| <span data-ttu-id="0d7e1-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d7e1-185">Requirement</span></span> | <span data-ttu-id="0d7e1-186">Wert</span><span class="sxs-lookup"><span data-stu-id="0d7e1-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7e1-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d7e1-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0d7e1-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d7e1-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d7e1-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d7e1-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0d7e1-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d7e1-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d7e1-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d7e1-191">Namespace</span></span><br/>                | <span data-ttu-id="0d7e1-192">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0d7e1-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0d7e1-193">Header</span><span class="sxs-lookup"><span data-stu-id="0d7e1-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d7e1-194"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d7e1-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="0d7e1-195">MOF</span><span class="sxs-lookup"><span data-stu-id="0d7e1-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d7e1-196"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d7e1-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d7e1-197">DLL</span><span class="sxs-lookup"><span data-stu-id="0d7e1-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d7e1-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d7e1-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d7e1-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d7e1-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7e1-200">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="0d7e1-201">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="0d7e1-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="0d7e1-202">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="0d7e1-203">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="0d7e1-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="0d7e1-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="0d7e1-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

