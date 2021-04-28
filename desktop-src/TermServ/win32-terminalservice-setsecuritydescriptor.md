---
title: SetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste)
description: 'SetSecurityDescriptor-Methode der Win32_Service-Klasse (Remotedesktopdienste): Schreibt eine aktualisierte Version des Sicherheitsdeskriptors, die den Zugriff auf den Dienst steuert.'
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- Scripting Windows-Verwaltungsinstrumentation , Sicherheit
- Sicherheit Windows-Verwaltungsinstrumentation , Skripterstellung
- SetSecurityDescriptor-Remotedesktopdienste
- SetSecurityDescriptor-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service klasse Remotedesktopdienste , SetSecurityDescriptor-Methode
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2dd7e43041c05b1c294181f8bd01548ed76d87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114492"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="93db7-108">SetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="93db7-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="93db7-109">Die **SetSecurityDescriptor-Methode** schreibt eine aktualisierte Version des Sicherheitsdeskriptors, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="93db7-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="93db7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="93db7-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="93db7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="93db7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93db7-112">*Deskriptor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="93db7-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93db7-113">Der dem Dienst zugeordnete Sicherheitsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="93db7-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93db7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93db7-114">Return value</span></span>

<span data-ttu-id="93db7-115">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93db7-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="93db7-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="93db7-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="93db7-117">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="93db7-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="93db7-118">**0**</span><span class="sxs-lookup"><span data-stu-id="93db7-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-119">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="93db7-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-120">**1**</span><span class="sxs-lookup"><span data-stu-id="93db7-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-121">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93db7-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-122">**2**</span><span class="sxs-lookup"><span data-stu-id="93db7-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-123">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="93db7-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-124">**3**</span><span class="sxs-lookup"><span data-stu-id="93db7-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-125">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="93db7-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-126">**4**</span><span class="sxs-lookup"><span data-stu-id="93db7-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-127">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="93db7-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-128">**5**</span><span class="sxs-lookup"><span data-stu-id="93db7-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-129">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="93db7-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-130">**6**</span><span class="sxs-lookup"><span data-stu-id="93db7-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-131">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="93db7-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-132">**7**</span><span class="sxs-lookup"><span data-stu-id="93db7-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-133">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="93db7-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-134">**8**</span><span class="sxs-lookup"><span data-stu-id="93db7-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-135">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="93db7-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-136">**9**</span><span class="sxs-lookup"><span data-stu-id="93db7-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-137">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="93db7-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-138">**10**</span><span class="sxs-lookup"><span data-stu-id="93db7-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-139">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93db7-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-140">**11**</span><span class="sxs-lookup"><span data-stu-id="93db7-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-141">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="93db7-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-142">**12**</span><span class="sxs-lookup"><span data-stu-id="93db7-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-143">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="93db7-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-144">**13**</span><span class="sxs-lookup"><span data-stu-id="93db7-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-145">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="93db7-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-146">**14**</span><span class="sxs-lookup"><span data-stu-id="93db7-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-147">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="93db7-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-148">**15**</span><span class="sxs-lookup"><span data-stu-id="93db7-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-149">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="93db7-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-150">**16**</span><span class="sxs-lookup"><span data-stu-id="93db7-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-151">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="93db7-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-152">**17**</span><span class="sxs-lookup"><span data-stu-id="93db7-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-153">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="93db7-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-154">**18**</span><span class="sxs-lookup"><span data-stu-id="93db7-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-155">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="93db7-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-156">**19**</span><span class="sxs-lookup"><span data-stu-id="93db7-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-157">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93db7-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-158">**20**</span><span class="sxs-lookup"><span data-stu-id="93db7-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-159">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="93db7-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-160">**21**</span><span class="sxs-lookup"><span data-stu-id="93db7-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-161">An den Dienst wurden ungültige Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="93db7-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-162">**22**</span><span class="sxs-lookup"><span data-stu-id="93db7-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-163">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="93db7-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-164">**23**</span><span class="sxs-lookup"><span data-stu-id="93db7-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-165">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93db7-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="93db7-166">**24**</span><span class="sxs-lookup"><span data-stu-id="93db7-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="93db7-167">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="93db7-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93db7-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93db7-168">Remarks</span></span>

<span data-ttu-id="93db7-169">Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine SACL [*(System Access Control List).*](/windows/desktop/SecGloss/s-gly)</span><span class="sxs-lookup"><span data-stu-id="93db7-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="93db7-170">Weitere Informationen finden Sie unter [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="93db7-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="93db7-171">Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="93db7-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="93db7-172">Weitere Informationen finden Sie unter [**Berechtigungskonstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge.](/windows/desktop/WmiSdk/executing-privileged-operations)</span><span class="sxs-lookup"><span data-stu-id="93db7-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="93db7-173">Sie können sowohl die DACL als auch die SACL in der [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) aktualisieren, wenn Sie diese Methode aufrufen. Sie können jedoch auch nur die DACL oder nur die SACL aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="93db7-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="93db7-174">Die folgenden Werte in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beide aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="93db7-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="93db7-175">**SE \_ DACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="93db7-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="93db7-176">Gibt an, dass die DACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="93db7-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="93db7-177">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.</span><span class="sxs-lookup"><span data-stu-id="93db7-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="93db7-178">**SE \_ SACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="93db7-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="93db7-179">Gibt an, dass die SACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="93db7-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="93db7-180">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei.</span><span class="sxs-lookup"><span data-stu-id="93db7-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="93db7-181">Zum Aktualisieren der SACL muss für das Konto die **SeSecurityPrivilege-Berechtigung** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="93db7-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="93db7-182">Für die Skripterstellung ist der Berechtigungsname **SeSecurityPrivilege.**</span><span class="sxs-lookup"><span data-stu-id="93db7-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="93db7-183">Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="93db7-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="93db7-184">Wenn der Gruppentreuhänder und die Eigenschaften des Besitzertreuhänders nicht **NULL sind,** werden sie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="93db7-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="93db7-185">Andernfalls behält WMI die ursprünglichen Werte bei.</span><span class="sxs-lookup"><span data-stu-id="93db7-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="93db7-186">Weitere Informationen finden Sie unter [WMI-Sicherheitsdeskriptorobjekte.](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)</span><span class="sxs-lookup"><span data-stu-id="93db7-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="93db7-187">Wenn eine neue SACL in einem Aufruf dieser Methode **NULL** ist, bleibt die Sicherheitsbeschreibung SACL für das sicherungsfähige Zielobjekt unverändert.</span><span class="sxs-lookup"><span data-stu-id="93db7-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="93db7-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93db7-188">Requirements</span></span>



| <span data-ttu-id="93db7-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93db7-189">Requirement</span></span> | <span data-ttu-id="93db7-190">Wert</span><span class="sxs-lookup"><span data-stu-id="93db7-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93db7-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93db7-191">Minimum supported client</span></span><br/> | <span data-ttu-id="93db7-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93db7-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93db7-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93db7-193">Minimum supported server</span></span><br/> | <span data-ttu-id="93db7-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93db7-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93db7-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="93db7-195">Namespace</span></span><br/>                | <span data-ttu-id="93db7-196">\\ \\ CiMv2-Stammterminaldienste</span><span class="sxs-lookup"><span data-stu-id="93db7-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="93db7-197">MOF</span><span class="sxs-lookup"><span data-stu-id="93db7-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93db7-198"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="93db7-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="93db7-199">DLL</span><span class="sxs-lookup"><span data-stu-id="93db7-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93db7-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93db7-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93db7-201">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="93db7-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93db7-202">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="93db7-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="93db7-203">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="93db7-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="93db7-204">**Berechtigungskonst constants**</span><span class="sxs-lookup"><span data-stu-id="93db7-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="93db7-205">WMI-Sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="93db7-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="93db7-206">Ändern der Zugriffssicherheit für sicherungsfähige Objekte</span><span class="sxs-lookup"><span data-stu-id="93db7-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="93db7-207">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="93db7-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

