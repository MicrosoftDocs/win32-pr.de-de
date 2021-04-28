---
description: 'GetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32-WMI-Anbieter): Gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert.'
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: GetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32-WMI-Anbieter)
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
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096988"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="d6d59-103">GetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="d6d59-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d6d59-104">Die **GetSecurityDescriptor-Methode** gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="d6d59-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="d6d59-105">Der Deskriptor wird als Instanz von [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6d59-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d59-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6d59-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d6d59-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6d59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d59-108">*Deskriptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d6d59-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-109">Der dem Dienst zugeordnete Sicherheitsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="d6d59-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d59-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6d59-110">Return value</span></span>

<span data-ttu-id="d6d59-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d6d59-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d6d59-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="d6d59-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d6d59-113">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="d6d59-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d6d59-114">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="d6d59-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-115">0</span><span class="sxs-lookup"><span data-stu-id="d6d59-115">0</span></span>

<span data-ttu-id="d6d59-116">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d6d59-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-117">1</span><span class="sxs-lookup"><span data-stu-id="d6d59-117">1</span></span>

<span data-ttu-id="d6d59-118">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d6d59-119">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="d6d59-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-120">2</span><span class="sxs-lookup"><span data-stu-id="d6d59-120">2</span></span>

<span data-ttu-id="d6d59-121">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="d6d59-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-122">3</span><span class="sxs-lookup"><span data-stu-id="d6d59-122">3</span></span>

<span data-ttu-id="d6d59-123">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d6d59-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-124">4</span><span class="sxs-lookup"><span data-stu-id="d6d59-124">4</span></span>

<span data-ttu-id="d6d59-125">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="d6d59-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-126">5</span><span class="sxs-lookup"><span data-stu-id="d6d59-126">5</span></span>

<span data-ttu-id="d6d59-127">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](win32-baseservice.md)) ist.**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="d6d59-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-128">6</span><span class="sxs-lookup"><span data-stu-id="d6d59-128">6</span></span>

<span data-ttu-id="d6d59-129">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d6d59-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-130">7</span><span class="sxs-lookup"><span data-stu-id="d6d59-130">7</span></span>

<span data-ttu-id="d6d59-131">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="d6d59-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d6d59-132">**Unbekannter Fehler**</span><span class="sxs-lookup"><span data-stu-id="d6d59-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-133">8</span><span class="sxs-lookup"><span data-stu-id="d6d59-133">8</span></span>

<span data-ttu-id="d6d59-134">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="d6d59-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6d59-135">**Berechtigung fehlt**</span><span class="sxs-lookup"><span data-stu-id="d6d59-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-136">9</span><span class="sxs-lookup"><span data-stu-id="d6d59-136">9</span></span>

<span data-ttu-id="d6d59-137">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d6d59-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-138">10</span><span class="sxs-lookup"><span data-stu-id="d6d59-138">10</span></span>

<span data-ttu-id="d6d59-139">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-140">11</span><span class="sxs-lookup"><span data-stu-id="d6d59-140">11</span></span>

<span data-ttu-id="d6d59-141">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-142">12</span><span class="sxs-lookup"><span data-stu-id="d6d59-142">12</span></span>

<span data-ttu-id="d6d59-143">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-144">13</span><span class="sxs-lookup"><span data-stu-id="d6d59-144">13</span></span>

<span data-ttu-id="d6d59-145">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6d59-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-146">14</span><span class="sxs-lookup"><span data-stu-id="d6d59-146">14</span></span>

<span data-ttu-id="d6d59-147">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6d59-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-148">15</span><span class="sxs-lookup"><span data-stu-id="d6d59-148">15</span></span>

<span data-ttu-id="d6d59-149">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="d6d59-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-150">16</span><span class="sxs-lookup"><span data-stu-id="d6d59-150">16</span></span>

<span data-ttu-id="d6d59-151">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-152">17</span><span class="sxs-lookup"><span data-stu-id="d6d59-152">17</span></span>

<span data-ttu-id="d6d59-153">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="d6d59-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-154">18</span><span class="sxs-lookup"><span data-stu-id="d6d59-154">18</span></span>

<span data-ttu-id="d6d59-155">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="d6d59-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-156">19</span><span class="sxs-lookup"><span data-stu-id="d6d59-156">19</span></span>

<span data-ttu-id="d6d59-157">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-158">20</span><span class="sxs-lookup"><span data-stu-id="d6d59-158">20</span></span>

<span data-ttu-id="d6d59-159">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d6d59-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d6d59-160">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="d6d59-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-161">21</span><span class="sxs-lookup"><span data-stu-id="d6d59-161">21</span></span>

<span data-ttu-id="d6d59-162">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="d6d59-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-163">22</span><span class="sxs-lookup"><span data-stu-id="d6d59-163">22</span></span>

<span data-ttu-id="d6d59-164">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="d6d59-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-165">23</span><span class="sxs-lookup"><span data-stu-id="d6d59-165">23</span></span>

<span data-ttu-id="d6d59-166">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d6d59-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6d59-167">24</span><span class="sxs-lookup"><span data-stu-id="d6d59-167">24</span></span>

<span data-ttu-id="d6d59-168">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="d6d59-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6d59-169">**Andere**</span><span class="sxs-lookup"><span data-stu-id="d6d59-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d6d59-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="d6d59-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6d59-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6d59-171">Remarks</span></span>

<span data-ttu-id="d6d59-172">Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine DACL (Discretionary [*Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly)</span><span class="sxs-lookup"><span data-stu-id="d6d59-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d6d59-173">Weitere Informationen finden Sie unter [Access Control Listen.](/windows/desktop/SecAuthZ/access-control-lists)</span><span class="sxs-lookup"><span data-stu-id="d6d59-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d6d59-174">Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6d59-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d6d59-175">Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) und [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d6d59-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="d6d59-176">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6d59-176">Examples</span></span>

<span data-ttu-id="d6d59-177">Achten Sie beim Abrufen eines Sicherheitsdeskriptors in VBScript darauf, dass Sie "Sicherheit" verwenden und als Administrator ausführen, wie im folgenden Codeausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6d59-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="d6d59-178">Andernfalls löst Ihr Code möglicherweise einen Berechtigungsfehler aus.</span><span class="sxs-lookup"><span data-stu-id="d6d59-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="d6d59-179">Ebenso müssen Sie in VB.NET sicherstellen, dass Sie "EnablePrivileges = True" festlegen und die Anwendung als Administrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6d59-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="d6d59-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6d59-180">Requirements</span></span>



| <span data-ttu-id="d6d59-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6d59-181">Requirement</span></span> | <span data-ttu-id="d6d59-182">Wert</span><span class="sxs-lookup"><span data-stu-id="d6d59-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d59-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6d59-183">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d59-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6d59-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6d59-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6d59-185">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d59-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6d59-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6d59-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6d59-187">Namespace</span></span><br/>                | <span data-ttu-id="d6d59-188">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="d6d59-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6d59-189">MOF</span><span class="sxs-lookup"><span data-stu-id="d6d59-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6d59-190"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6d59-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6d59-191">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d59-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d59-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d59-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d59-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6d59-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d59-194">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="d6d59-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="d6d59-195">**Berechtigungskonst constants**</span><span class="sxs-lookup"><span data-stu-id="d6d59-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="d6d59-196">WMI-Sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="d6d59-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="d6d59-197">Ändern der Zugriffssicherheit für sicherungsfähige Objekte</span><span class="sxs-lookup"><span data-stu-id="d6d59-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="d6d59-198">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="d6d59-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

