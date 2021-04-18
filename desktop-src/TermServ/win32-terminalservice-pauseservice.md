---
title: PauseService-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Versucht, den Dienst anzuhalten.
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der PauseService-Methode
- Win32_Service-Klasse der PauseService-Methode Remotedesktopdienste
- Win32_Service-Klasse Remotedesktopdienste, PauseService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69951a77530b3aff89148b08e19f3a7c4da8f5b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338718"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="ac565-106">PauseService-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="ac565-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="ac565-107">Die " **PauseService** "- [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, den Dienst im angehaltenen Zustand zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="ac565-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="ac565-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac565-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ac565-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ac565-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac565-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac565-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="ac565-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac565-111">Parameters</span></span>

<span data-ttu-id="ac565-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ac565-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac565-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac565-113">Return value</span></span>

<span data-ttu-id="ac565-114">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ac565-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ac565-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ac565-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ac565-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ac565-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ac565-117">**0**</span><span class="sxs-lookup"><span data-stu-id="ac565-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-118">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="ac565-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-119">**1**</span><span class="sxs-lookup"><span data-stu-id="ac565-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-120">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac565-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-121">**2**</span><span class="sxs-lookup"><span data-stu-id="ac565-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-122">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="ac565-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-123">**3**</span><span class="sxs-lookup"><span data-stu-id="ac565-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-124">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ac565-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-125">**4**</span><span class="sxs-lookup"><span data-stu-id="ac565-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="ac565-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-127">**5**</span><span class="sxs-lookup"><span data-stu-id="ac565-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-128">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="ac565-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-129">**6**</span><span class="sxs-lookup"><span data-stu-id="ac565-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-130">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="ac565-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-131">**7**</span><span class="sxs-lookup"><span data-stu-id="ac565-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-132">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="ac565-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-133">**8**</span><span class="sxs-lookup"><span data-stu-id="ac565-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-134">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ac565-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-135">**9**</span><span class="sxs-lookup"><span data-stu-id="ac565-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-136">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ac565-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-137">**10**</span><span class="sxs-lookup"><span data-stu-id="ac565-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac565-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-139">**11**</span><span class="sxs-lookup"><span data-stu-id="ac565-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="ac565-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-141">**12**</span><span class="sxs-lookup"><span data-stu-id="ac565-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-142">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac565-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-143">**13**</span><span class="sxs-lookup"><span data-stu-id="ac565-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ac565-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-145">**14**</span><span class="sxs-lookup"><span data-stu-id="ac565-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac565-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-147">**15**</span><span class="sxs-lookup"><span data-stu-id="ac565-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ac565-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-149">**16**</span><span class="sxs-lookup"><span data-stu-id="ac565-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac565-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-151">**17**</span><span class="sxs-lookup"><span data-stu-id="ac565-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-152">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="ac565-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-153">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="ac565-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-154">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ac565-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-155">**19**</span><span class="sxs-lookup"><span data-stu-id="ac565-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-156">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac565-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-157">**20**</span><span class="sxs-lookup"><span data-stu-id="ac565-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-158">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ac565-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-159">**21**</span><span class="sxs-lookup"><span data-stu-id="ac565-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-160">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ac565-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-161">**22**</span><span class="sxs-lookup"><span data-stu-id="ac565-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-162">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ac565-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-163">**23**</span><span class="sxs-lookup"><span data-stu-id="ac565-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-164">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac565-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ac565-165">**24**</span><span class="sxs-lookup"><span data-stu-id="ac565-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ac565-166">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="ac565-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac565-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac565-167">Remarks</span></span>

<span data-ttu-id="ac565-168">Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die-Methode [**StopService**](win32-terminalservice-stopservice.md) und die **anhaleservice** -Methode verwenden, um-Dienste anzuhalten und anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="ac565-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="ac565-169">Die Entscheidung, einen Dienst zu stoppen, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="ac565-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="ac565-170">Ist der Dienst in der Lage, angehalten zu werden?</span><span class="sxs-lookup"><span data-stu-id="ac565-170">Is the service capable of being paused?</span></span> <span data-ttu-id="ac565-171">Wenn dies nicht der Wert ist, ist die einzige Option der Dienst wird beendet.</span><span class="sxs-lookup"><span data-stu-id="ac565-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="ac565-172">Müssen Sie die Verarbeitung von Client Anforderungen für alle Benutzer fortsetzen, die bereits mit dem Dienst verbunden sind?</span><span class="sxs-lookup"><span data-stu-id="ac565-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="ac565-173">Wenn dies der Fall ist, ermöglicht das Anhalten eines Dienstanbieter in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert</span><span class="sxs-lookup"><span data-stu-id="ac565-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="ac565-174">Wenn Sie einen Dienst beenden, werden dagegen alle Clients sofort getrennt.</span><span class="sxs-lookup"><span data-stu-id="ac565-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="ac565-175">Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden?</span><span class="sxs-lookup"><span data-stu-id="ac565-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="ac565-176">Obwohl Dienst Eigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten nicht wirksam, bis der Dienst tatsächlich beendet und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ac565-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="ac565-177">Der zum Anhalten eines Dienstanbieter erforderliche Skriptcode ist nahezu identisch mit dem Code, der zum Anhalten des Dienstanbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ac565-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="ac565-178">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac565-178">Examples</span></span>

<span data-ttu-id="ac565-179">Die [Unterbrechungs Dienste, die unter einem bestimmten Konto](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript-Beispiel ausgeführt werden, halten alle Dienste an, die unter dem hypothetischen Dienst Konto "netzvc</span><span class="sxs-lookup"><span data-stu-id="ac565-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac565-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac565-180">Requirements</span></span>



| <span data-ttu-id="ac565-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac565-181">Requirement</span></span> | <span data-ttu-id="ac565-182">Wert</span><span class="sxs-lookup"><span data-stu-id="ac565-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac565-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac565-183">Minimum supported client</span></span><br/> | <span data-ttu-id="ac565-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac565-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac565-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac565-185">Minimum supported server</span></span><br/> | <span data-ttu-id="ac565-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac565-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac565-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac565-187">Namespace</span></span><br/>                | <span data-ttu-id="ac565-188">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ac565-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ac565-189">MOF</span><span class="sxs-lookup"><span data-stu-id="ac565-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac565-190"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac565-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac565-191">DLL</span><span class="sxs-lookup"><span data-stu-id="ac565-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac565-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac565-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac565-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac565-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac565-194">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="ac565-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="ac565-195">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="ac565-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="ac565-196">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="ac565-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="ac565-197">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="ac565-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="ac565-198">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="ac565-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

