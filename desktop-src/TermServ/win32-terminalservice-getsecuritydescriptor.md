---
title: GetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste)
description: 'GetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste): Gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert.'
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- Scripting Windows-Verwaltungsinstrumentation , Sicherheit
- Sicherheit Windows-Verwaltungsinstrumentation , Skripterstellung
- GetSecurityDescriptor-Remotedesktopdienste
- GetSecurityDescriptor-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service klasse Remotedesktopdienste , GetSecurityDescriptor-Methode
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
ms.openlocfilehash: ea5b8a9b945048f947aa273e1ccc1f4514469681
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090648"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="27707-108">GetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="27707-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="27707-109">Die **GetSecurityDescriptor-Methode** gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="27707-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="27707-110">Der Deskriptor wird als Instanz von [**Win32 \_ SecurityDescriptor zurückgegeben.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)</span><span class="sxs-lookup"><span data-stu-id="27707-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="27707-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="27707-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="27707-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="27707-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27707-113">*Deskriptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27707-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27707-114">Der dem Dienst zugeordnete Sicherheitsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="27707-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27707-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27707-115">Return value</span></span>

<span data-ttu-id="27707-116">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="27707-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="27707-117">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="27707-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="27707-118">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="27707-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="27707-119">**0**</span><span class="sxs-lookup"><span data-stu-id="27707-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="27707-120">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="27707-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="27707-121">**1**</span><span class="sxs-lookup"><span data-stu-id="27707-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="27707-122">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27707-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="27707-123">**2**</span><span class="sxs-lookup"><span data-stu-id="27707-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="27707-124">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="27707-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="27707-125">**3**</span><span class="sxs-lookup"><span data-stu-id="27707-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="27707-126">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="27707-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="27707-127">**4**</span><span class="sxs-lookup"><span data-stu-id="27707-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="27707-128">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="27707-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="27707-129">**5**</span><span class="sxs-lookup"><span data-stu-id="27707-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="27707-130">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="27707-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="27707-131">**6**</span><span class="sxs-lookup"><span data-stu-id="27707-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="27707-132">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="27707-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="27707-133">**7**</span><span class="sxs-lookup"><span data-stu-id="27707-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="27707-134">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="27707-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="27707-135">**8**</span><span class="sxs-lookup"><span data-stu-id="27707-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="27707-136">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="27707-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="27707-137">**9**</span><span class="sxs-lookup"><span data-stu-id="27707-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="27707-138">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="27707-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="27707-139">**10**</span><span class="sxs-lookup"><span data-stu-id="27707-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="27707-140">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27707-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="27707-141">**11**</span><span class="sxs-lookup"><span data-stu-id="27707-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="27707-142">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="27707-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="27707-143">**12**</span><span class="sxs-lookup"><span data-stu-id="27707-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="27707-144">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="27707-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27707-145">**13**</span><span class="sxs-lookup"><span data-stu-id="27707-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="27707-146">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="27707-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="27707-147">**14**</span><span class="sxs-lookup"><span data-stu-id="27707-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="27707-148">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="27707-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27707-149">**15**</span><span class="sxs-lookup"><span data-stu-id="27707-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="27707-150">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="27707-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="27707-151">**16**</span><span class="sxs-lookup"><span data-stu-id="27707-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="27707-152">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="27707-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27707-153">**17**</span><span class="sxs-lookup"><span data-stu-id="27707-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="27707-154">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="27707-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="27707-155">**18**</span><span class="sxs-lookup"><span data-stu-id="27707-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="27707-156">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="27707-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="27707-157">**19**</span><span class="sxs-lookup"><span data-stu-id="27707-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="27707-158">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27707-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="27707-159">**20**</span><span class="sxs-lookup"><span data-stu-id="27707-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="27707-160">Der Dienstname weist ungültige Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="27707-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="27707-161">**21**</span><span class="sxs-lookup"><span data-stu-id="27707-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="27707-162">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="27707-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="27707-163">**22**</span><span class="sxs-lookup"><span data-stu-id="27707-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="27707-164">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="27707-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="27707-165">**23**</span><span class="sxs-lookup"><span data-stu-id="27707-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="27707-166">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="27707-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27707-167">**24**</span><span class="sxs-lookup"><span data-stu-id="27707-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="27707-168">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="27707-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27707-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27707-169">Remarks</span></span>

<span data-ttu-id="27707-170">Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine SACL [*(System Access Control List).*](/windows/desktop/SecGloss/s-gly)</span><span class="sxs-lookup"><span data-stu-id="27707-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="27707-171">Weitere Informationen finden Sie unter [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="27707-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="27707-172">Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27707-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="27707-173">Weitere Informationen finden Sie unter [**Berechtigungskonstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge.](/windows/desktop/WmiSdk/executing-privileged-operations)</span><span class="sxs-lookup"><span data-stu-id="27707-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="27707-174">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27707-174">Examples</span></span>

<span data-ttu-id="27707-175">Achten Sie beim Abrufen eines Sicherheitsdeskriptors in VBScript darauf, "Sicherheit" zu verwenden und als Administrator auszuführen, wie im folgenden Codeausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="27707-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="27707-176">Andernfalls kann Ihr Code einen Berechtigungsfehler auslösen.</span><span class="sxs-lookup"><span data-stu-id="27707-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="27707-177">Achten Sie in VB.NET auf "EnablePrivileges = True", und führen Sie die Anwendung als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="27707-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="27707-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27707-178">Requirements</span></span>



| <span data-ttu-id="27707-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27707-179">Requirement</span></span> | <span data-ttu-id="27707-180">Wert</span><span class="sxs-lookup"><span data-stu-id="27707-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27707-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27707-181">Minimum supported client</span></span><br/> | <span data-ttu-id="27707-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27707-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27707-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27707-183">Minimum supported server</span></span><br/> | <span data-ttu-id="27707-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27707-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27707-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="27707-185">Namespace</span></span><br/>                | <span data-ttu-id="27707-186">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="27707-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="27707-187">MOF</span><span class="sxs-lookup"><span data-stu-id="27707-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27707-188"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="27707-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="27707-189">DLL</span><span class="sxs-lookup"><span data-stu-id="27707-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27707-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27707-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27707-191">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27707-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27707-192">**\_Win32-Dienst**</span><span class="sxs-lookup"><span data-stu-id="27707-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="27707-193">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="27707-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="27707-194">**Berechtigungskonst constants**</span><span class="sxs-lookup"><span data-stu-id="27707-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="27707-195">WMI-Sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="27707-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="27707-196">Ändern der Zugriffssicherheit für sicherungsfähige Objekte</span><span class="sxs-lookup"><span data-stu-id="27707-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="27707-197">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="27707-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

