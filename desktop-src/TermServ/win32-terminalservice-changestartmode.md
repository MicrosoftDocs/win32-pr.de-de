---
title: ChangeStartMode-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Ändert den Start Modus eines Win32 \_ Terminalservice.
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- ChangeStartMode-Methode Remotedesktopdienste
- ChangeStartMode-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, ChangeStartMode-Methode
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342425"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="c03ab-106">ChangeStartMode-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="c03ab-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="c03ab-107">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **ChangeStartMode** ändert den Start Modus eines [**Win32 \_ Terminalservice**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="c03ab-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="c03ab-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c03ab-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c03ab-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c03ab-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c03ab-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c03ab-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="c03ab-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c03ab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03ab-112">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c03ab-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-113">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c03ab-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="c03ab-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Starten**</span><span class="sxs-lookup"><span data-stu-id="c03ab-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="c03ab-115">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="c03ab-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="c03ab-116">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="c03ab-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="c03ab-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Anlage**</span><span class="sxs-lookup"><span data-stu-id="c03ab-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="c03ab-118">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="c03ab-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c03ab-119">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="c03ab-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="c03ab-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**</span><span class="sxs-lookup"><span data-stu-id="c03ab-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="c03ab-121">Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c03ab-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="c03ab-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**</span><span class="sxs-lookup"><span data-stu-id="c03ab-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="c03ab-123">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](win32-terminalservice-startservice.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="c03ab-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c03ab-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="c03ab-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="c03ab-125">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c03ab-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03ab-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c03ab-126">Return value</span></span>

<span data-ttu-id="c03ab-127">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c03ab-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="c03ab-128">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c03ab-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c03ab-129">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c03ab-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c03ab-130">**0**</span><span class="sxs-lookup"><span data-stu-id="c03ab-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-131">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c03ab-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-132">**1**</span><span class="sxs-lookup"><span data-stu-id="c03ab-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-133">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-134">**2**</span><span class="sxs-lookup"><span data-stu-id="c03ab-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-135">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c03ab-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-136">**3**</span><span class="sxs-lookup"><span data-stu-id="c03ab-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-137">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c03ab-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-138">**4**</span><span class="sxs-lookup"><span data-stu-id="c03ab-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-139">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="c03ab-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-140">**5**</span><span class="sxs-lookup"><span data-stu-id="c03ab-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-141">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="c03ab-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-142">**6**</span><span class="sxs-lookup"><span data-stu-id="c03ab-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-143">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c03ab-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-144">**7**</span><span class="sxs-lookup"><span data-stu-id="c03ab-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-145">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="c03ab-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-146">**8**</span><span class="sxs-lookup"><span data-stu-id="c03ab-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-147">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c03ab-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-148">**9**</span><span class="sxs-lookup"><span data-stu-id="c03ab-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-149">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c03ab-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-150">**10**</span><span class="sxs-lookup"><span data-stu-id="c03ab-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-151">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-152">**11**</span><span class="sxs-lookup"><span data-stu-id="c03ab-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-153">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-154">**12**</span><span class="sxs-lookup"><span data-stu-id="c03ab-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-155">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-156">**13**</span><span class="sxs-lookup"><span data-stu-id="c03ab-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-157">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c03ab-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-158">**14**</span><span class="sxs-lookup"><span data-stu-id="c03ab-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-159">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c03ab-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-160">**15**</span><span class="sxs-lookup"><span data-stu-id="c03ab-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-161">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c03ab-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-162">**16**</span><span class="sxs-lookup"><span data-stu-id="c03ab-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-163">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-164">**17**</span><span class="sxs-lookup"><span data-stu-id="c03ab-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-165">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="c03ab-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-166">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="c03ab-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-167">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c03ab-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-168">**19**</span><span class="sxs-lookup"><span data-stu-id="c03ab-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-169">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-170">**20**</span><span class="sxs-lookup"><span data-stu-id="c03ab-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-171">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c03ab-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-172">**21**</span><span class="sxs-lookup"><span data-stu-id="c03ab-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-173">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c03ab-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-174">**22**</span><span class="sxs-lookup"><span data-stu-id="c03ab-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-175">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c03ab-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-176">**23**</span><span class="sxs-lookup"><span data-stu-id="c03ab-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-177">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c03ab-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c03ab-178">**24**</span><span class="sxs-lookup"><span data-stu-id="c03ab-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c03ab-179">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="c03ab-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c03ab-180">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c03ab-180">Examples</span></span>

<span data-ttu-id="c03ab-181">Im folgenden wird der Start Modus eines Dienstanbieter geändert, wenn der Start [Modus eines Dienst](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) -PowerShell-Beispiels aus der TechNet Gallery abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c03ab-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="c03ab-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c03ab-182">Requirements</span></span>



| <span data-ttu-id="c03ab-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c03ab-183">Requirement</span></span> | <span data-ttu-id="c03ab-184">Wert</span><span class="sxs-lookup"><span data-stu-id="c03ab-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c03ab-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c03ab-185">Minimum supported client</span></span><br/> | <span data-ttu-id="c03ab-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c03ab-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c03ab-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c03ab-187">Minimum supported server</span></span><br/> | <span data-ttu-id="c03ab-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c03ab-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c03ab-189">Namespace</span><span class="sxs-lookup"><span data-stu-id="c03ab-189">Namespace</span></span><br/>                | <span data-ttu-id="c03ab-190">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c03ab-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c03ab-191">MOF</span><span class="sxs-lookup"><span data-stu-id="c03ab-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c03ab-192"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c03ab-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c03ab-193">DLL</span><span class="sxs-lookup"><span data-stu-id="c03ab-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c03ab-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c03ab-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03ab-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c03ab-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03ab-196">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c03ab-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="c03ab-197">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="c03ab-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="c03ab-198">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="c03ab-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="c03ab-199">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="c03ab-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

