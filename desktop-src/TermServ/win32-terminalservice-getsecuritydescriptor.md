---
title: Getsecuritydescriptor-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- Skripterstellung Windows-Verwaltungsinstrumentation, Sicherheit
- Sicherheits Windows-Verwaltungsinstrumentation, Skripterstellung
- Getsecuritydescriptor-Methode Remotedesktopdienste
- Getsecuritydescriptor-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, getsecuritydescriptor-Methode
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8dc271d5498163352af10bcb0b9c55e2e81fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949736"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="fbf53-108">Getsecuritydescriptor-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="fbf53-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="fbf53-109">Die **getsecuritydescriptor** -Methode gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="fbf53-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="fbf53-110">Der Deskriptor wird als eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fbf53-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf53-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf53-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="fbf53-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbf53-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf53-113">*Deskriptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fbf53-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-114">Die Sicherheits Beschreibung, die dem Dienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fbf53-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf53-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbf53-115">Return value</span></span>

<span data-ttu-id="fbf53-116">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fbf53-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="fbf53-117">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fbf53-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fbf53-118">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fbf53-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fbf53-119">**0**</span><span class="sxs-lookup"><span data-stu-id="fbf53-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-120">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fbf53-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-121">**1**</span><span class="sxs-lookup"><span data-stu-id="fbf53-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-122">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-123">**2**</span><span class="sxs-lookup"><span data-stu-id="fbf53-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-124">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="fbf53-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-125">**3**</span><span class="sxs-lookup"><span data-stu-id="fbf53-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-126">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="fbf53-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-127">**4**</span><span class="sxs-lookup"><span data-stu-id="fbf53-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-128">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="fbf53-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-129">**5**</span><span class="sxs-lookup"><span data-stu-id="fbf53-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-130">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="fbf53-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-131">**6**</span><span class="sxs-lookup"><span data-stu-id="fbf53-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-132">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="fbf53-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-133">**7**</span><span class="sxs-lookup"><span data-stu-id="fbf53-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-134">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="fbf53-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-135">**8**</span><span class="sxs-lookup"><span data-stu-id="fbf53-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-136">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="fbf53-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-137">**9**</span><span class="sxs-lookup"><span data-stu-id="fbf53-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-138">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="fbf53-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-139">**10**</span><span class="sxs-lookup"><span data-stu-id="fbf53-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-140">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-141">**11**</span><span class="sxs-lookup"><span data-stu-id="fbf53-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-142">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-143">**12**</span><span class="sxs-lookup"><span data-stu-id="fbf53-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-144">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-145">**13**</span><span class="sxs-lookup"><span data-stu-id="fbf53-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-146">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="fbf53-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-147">**14**</span><span class="sxs-lookup"><span data-stu-id="fbf53-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-148">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fbf53-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-149">**15**</span><span class="sxs-lookup"><span data-stu-id="fbf53-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-150">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="fbf53-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-151">**16**</span><span class="sxs-lookup"><span data-stu-id="fbf53-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-152">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-153">**17**</span><span class="sxs-lookup"><span data-stu-id="fbf53-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-154">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="fbf53-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-155">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="fbf53-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-156">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fbf53-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-157">**19**</span><span class="sxs-lookup"><span data-stu-id="fbf53-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-158">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-159">**20**</span><span class="sxs-lookup"><span data-stu-id="fbf53-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-160">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fbf53-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-161">**21**</span><span class="sxs-lookup"><span data-stu-id="fbf53-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-162">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-163">**22**</span><span class="sxs-lookup"><span data-stu-id="fbf53-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-164">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="fbf53-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-165">**23**</span><span class="sxs-lookup"><span data-stu-id="fbf53-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-166">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fbf53-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fbf53-167">**24**</span><span class="sxs-lookup"><span data-stu-id="fbf53-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="fbf53-168">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="fbf53-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbf53-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbf53-169">Remarks</span></span>

<span data-ttu-id="fbf53-170">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="fbf53-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="fbf53-171">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="fbf53-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="fbf53-172">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fbf53-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="fbf53-173">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="fbf53-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="fbf53-174">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbf53-174">Examples</span></span>

<span data-ttu-id="fbf53-175">Wenn Sie eine Sicherheits Beschreibung in VBScript abrufen, achten Sie darauf, dass Sie "Sicherheit" ausführen und als Administrator ausführen, wie im folgenden Code Ausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fbf53-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="fbf53-176">Andernfalls löst der Code möglicherweise einen Berechtigungs Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="fbf53-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="fbf53-177">Legen Sie auf ähnliche Weise in VB.net "enableprivileges = true" fest, und führen Sie die Anwendung als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="fbf53-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="fbf53-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf53-178">Requirements</span></span>



| <span data-ttu-id="fbf53-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf53-179">Requirement</span></span> | <span data-ttu-id="fbf53-180">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf53-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf53-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbf53-181">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf53-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbf53-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbf53-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbf53-183">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf53-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbf53-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbf53-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbf53-185">Namespace</span></span><br/>                | <span data-ttu-id="fbf53-186">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fbf53-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fbf53-187">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf53-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf53-188"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fbf53-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf53-189">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf53-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf53-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf53-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf53-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf53-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf53-192">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="fbf53-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="fbf53-193">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="fbf53-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="fbf53-194">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="fbf53-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="fbf53-195">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="fbf53-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="fbf53-196">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="fbf53-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="fbf53-197">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="fbf53-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

