---
description: Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Getsecuritydescriptor-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041395"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="d5787-103">Getsecuritydescriptor-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="d5787-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d5787-104">Die **getsecuritydescriptor** -Methode gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="d5787-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="d5787-105">Der Deskriptor wird als eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5787-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5787-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5787-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d5787-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5787-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5787-108">*Deskriptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5787-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5787-109">Die Sicherheits Beschreibung, die dem Dienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d5787-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5787-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5787-110">Return value</span></span>

<span data-ttu-id="d5787-111">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d5787-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d5787-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d5787-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d5787-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d5787-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d5787-114">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="d5787-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d5787-115">0</span><span class="sxs-lookup"><span data-stu-id="d5787-115">0</span></span>

<span data-ttu-id="d5787-116">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d5787-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-117">1</span><span class="sxs-lookup"><span data-stu-id="d5787-117">1</span></span>

<span data-ttu-id="d5787-118">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5787-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d5787-119">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="d5787-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d5787-120">2</span><span class="sxs-lookup"><span data-stu-id="d5787-120">2</span></span>

<span data-ttu-id="d5787-121">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="d5787-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-122">3</span><span class="sxs-lookup"><span data-stu-id="d5787-122">3</span></span>

<span data-ttu-id="d5787-123">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d5787-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-124">4</span><span class="sxs-lookup"><span data-stu-id="d5787-124">4</span></span>

<span data-ttu-id="d5787-125">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="d5787-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-126">5</span><span class="sxs-lookup"><span data-stu-id="d5787-126">5</span></span>

<span data-ttu-id="d5787-127">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="d5787-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-128">6</span><span class="sxs-lookup"><span data-stu-id="d5787-128">6</span></span>

<span data-ttu-id="d5787-129">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d5787-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-130">7</span><span class="sxs-lookup"><span data-stu-id="d5787-130">7</span></span>

<span data-ttu-id="d5787-131">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="d5787-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d5787-132">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d5787-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d5787-133">8</span><span class="sxs-lookup"><span data-stu-id="d5787-133">8</span></span>

<span data-ttu-id="d5787-134">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d5787-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5787-135">**Fehlende Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="d5787-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="d5787-136">9</span><span class="sxs-lookup"><span data-stu-id="d5787-136">9</span></span>

<span data-ttu-id="d5787-137">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d5787-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-138">10</span><span class="sxs-lookup"><span data-stu-id="d5787-138">10</span></span>

<span data-ttu-id="d5787-139">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5787-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-140">11</span><span class="sxs-lookup"><span data-stu-id="d5787-140">11</span></span>

<span data-ttu-id="d5787-141">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d5787-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-142">12</span><span class="sxs-lookup"><span data-stu-id="d5787-142">12</span></span>

<span data-ttu-id="d5787-143">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5787-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-144">13</span><span class="sxs-lookup"><span data-stu-id="d5787-144">13</span></span>

<span data-ttu-id="d5787-145">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5787-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-146">14</span><span class="sxs-lookup"><span data-stu-id="d5787-146">14</span></span>

<span data-ttu-id="d5787-147">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5787-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-148">15</span><span class="sxs-lookup"><span data-stu-id="d5787-148">15</span></span>

<span data-ttu-id="d5787-149">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="d5787-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-150">16</span><span class="sxs-lookup"><span data-stu-id="d5787-150">16</span></span>

<span data-ttu-id="d5787-151">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5787-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-152">17</span><span class="sxs-lookup"><span data-stu-id="d5787-152">17</span></span>

<span data-ttu-id="d5787-153">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="d5787-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-154">18</span><span class="sxs-lookup"><span data-stu-id="d5787-154">18</span></span>

<span data-ttu-id="d5787-155">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d5787-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-156">19</span><span class="sxs-lookup"><span data-stu-id="d5787-156">19</span></span>

<span data-ttu-id="d5787-157">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5787-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-158">20</span><span class="sxs-lookup"><span data-stu-id="d5787-158">20</span></span>

<span data-ttu-id="d5787-159">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5787-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d5787-160">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="d5787-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d5787-161">21</span><span class="sxs-lookup"><span data-stu-id="d5787-161">21</span></span>

<span data-ttu-id="d5787-162">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d5787-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-163">22</span><span class="sxs-lookup"><span data-stu-id="d5787-163">22</span></span>

<span data-ttu-id="d5787-164">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d5787-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-165">23</span><span class="sxs-lookup"><span data-stu-id="d5787-165">23</span></span>

<span data-ttu-id="d5787-166">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d5787-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5787-167">24</span><span class="sxs-lookup"><span data-stu-id="d5787-167">24</span></span>

<span data-ttu-id="d5787-168">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="d5787-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5787-169">**Andere**</span><span class="sxs-lookup"><span data-stu-id="d5787-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d5787-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="d5787-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5787-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5787-171">Remarks</span></span>

<span data-ttu-id="d5787-172">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d5787-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d5787-173">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="d5787-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d5787-174">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5787-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d5787-175">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d5787-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="d5787-176">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5787-176">Examples</span></span>

<span data-ttu-id="d5787-177">Wenn Sie eine Sicherheits Beschreibung in VBScript abrufen, achten Sie darauf, dass Sie "Sicherheit" ausführen und als Administrator ausführen, wie im folgenden Code Ausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5787-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="d5787-178">Andernfalls löst der Code möglicherweise einen Berechtigungs Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="d5787-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="d5787-179">Legen Sie auf ähnliche Weise in VB.net "enableprivileges = true" fest, und führen Sie die Anwendung als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="d5787-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="d5787-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5787-180">Requirements</span></span>



| <span data-ttu-id="d5787-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5787-181">Requirement</span></span> | <span data-ttu-id="d5787-182">Wert</span><span class="sxs-lookup"><span data-stu-id="d5787-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5787-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5787-183">Minimum supported client</span></span><br/> | <span data-ttu-id="d5787-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5787-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5787-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5787-185">Minimum supported server</span></span><br/> | <span data-ttu-id="d5787-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5787-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5787-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5787-187">Namespace</span></span><br/>                | <span data-ttu-id="d5787-188">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d5787-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5787-189">MOF</span><span class="sxs-lookup"><span data-stu-id="d5787-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5787-190"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d5787-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5787-191">DLL</span><span class="sxs-lookup"><span data-stu-id="d5787-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5787-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5787-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5787-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5787-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5787-194">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="d5787-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="d5787-195">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="d5787-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="d5787-196">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="d5787-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="d5787-197">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="d5787-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="d5787-198">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="d5787-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

