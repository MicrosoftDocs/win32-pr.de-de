---
description: 'SetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32 WMI-Anbieter): Schreibt eine aktualisierte Version des Sicherheitsdeskriptors, die den Zugriff auf den Dienst steuert.'
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: SetSecurityDescriptor-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20619a459171841d0a3bd5b7acabe984dc835dac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100005"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="1aa71-103">SetSecurityDescriptor-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="1aa71-103">SetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1aa71-104">Die **SetSecurityDescriptor-Methode** schreibt eine aktualisierte Version des Sicherheitsdeskriptors, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="1aa71-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aa71-105">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="1aa71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aa71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa71-107">*Deskriptor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1aa71-107">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-108">Der dem Dienst zugeordnete Sicherheitsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="1aa71-108">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa71-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aa71-109">Return value</span></span>

<span data-ttu-id="1aa71-110">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1aa71-110">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="1aa71-111">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1aa71-111">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1aa71-112">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1aa71-112">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1aa71-113">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="1aa71-113">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-114">0</span><span class="sxs-lookup"><span data-stu-id="1aa71-114">0</span></span>

<span data-ttu-id="1aa71-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1aa71-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-116">**1**</span><span class="sxs-lookup"><span data-stu-id="1aa71-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1aa71-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-118">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="1aa71-118">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-119">2</span><span class="sxs-lookup"><span data-stu-id="1aa71-119">2</span></span>

<span data-ttu-id="1aa71-120">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="1aa71-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-121">**3**</span><span class="sxs-lookup"><span data-stu-id="1aa71-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-122">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="1aa71-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-123">**4**</span><span class="sxs-lookup"><span data-stu-id="1aa71-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-124">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="1aa71-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-125">**5**</span><span class="sxs-lookup"><span data-stu-id="1aa71-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-126">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="1aa71-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-127">**6**</span><span class="sxs-lookup"><span data-stu-id="1aa71-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-128">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="1aa71-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-129">**7**</span><span class="sxs-lookup"><span data-stu-id="1aa71-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-130">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="1aa71-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-131">**Unbekannter Fehler**</span><span class="sxs-lookup"><span data-stu-id="1aa71-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-132">8</span><span class="sxs-lookup"><span data-stu-id="1aa71-132">8</span></span>

<span data-ttu-id="1aa71-133">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1aa71-133">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-134">**Berechtigung fehlt**</span><span class="sxs-lookup"><span data-stu-id="1aa71-134">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-135">9</span><span class="sxs-lookup"><span data-stu-id="1aa71-135">9</span></span>

<span data-ttu-id="1aa71-136">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1aa71-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-137">**10**</span><span class="sxs-lookup"><span data-stu-id="1aa71-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1aa71-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-139">**11**</span><span class="sxs-lookup"><span data-stu-id="1aa71-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1aa71-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-141">**12**</span><span class="sxs-lookup"><span data-stu-id="1aa71-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-142">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="1aa71-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-143">**13**</span><span class="sxs-lookup"><span data-stu-id="1aa71-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1aa71-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-145">**14**</span><span class="sxs-lookup"><span data-stu-id="1aa71-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1aa71-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-147">**15**</span><span class="sxs-lookup"><span data-stu-id="1aa71-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1aa71-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-149">**16**</span><span class="sxs-lookup"><span data-stu-id="1aa71-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="1aa71-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-151">**17**</span><span class="sxs-lookup"><span data-stu-id="1aa71-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-152">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="1aa71-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-153">**18**</span><span class="sxs-lookup"><span data-stu-id="1aa71-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-154">Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="1aa71-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-155">**19**</span><span class="sxs-lookup"><span data-stu-id="1aa71-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-156">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1aa71-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-157">**20**</span><span class="sxs-lookup"><span data-stu-id="1aa71-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-158">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1aa71-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-159">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="1aa71-159">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-160">21</span><span class="sxs-lookup"><span data-stu-id="1aa71-160">21</span></span>

<span data-ttu-id="1aa71-161">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="1aa71-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-162">**22**</span><span class="sxs-lookup"><span data-stu-id="1aa71-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-163">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1aa71-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-164">**23**</span><span class="sxs-lookup"><span data-stu-id="1aa71-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-165">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1aa71-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-166">**24**</span><span class="sxs-lookup"><span data-stu-id="1aa71-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-167">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="1aa71-167">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aa71-168">**Andere**</span><span class="sxs-lookup"><span data-stu-id="1aa71-168">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1aa71-169">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="1aa71-169">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1aa71-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aa71-170">Remarks</span></span>

<span data-ttu-id="1aa71-171">Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine SACL [*(System Access Control List).*](/windows/desktop/SecGloss/s-gly)</span><span class="sxs-lookup"><span data-stu-id="1aa71-171">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="1aa71-172">Weitere Informationen finden Sie unter [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="1aa71-172">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="1aa71-173">Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1aa71-173">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="1aa71-174">Weitere Informationen finden Sie unter [**Berechtigungskonstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge.](/windows/desktop/WmiSdk/executing-privileged-operations)</span><span class="sxs-lookup"><span data-stu-id="1aa71-174">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="1aa71-175">Sie können sowohl die DACL als auch die SACL in der [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) aktualisieren, wenn Sie diese Methode aufrufen. Sie können jedoch auch nur die DACL oder nur die SACL aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1aa71-175">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="1aa71-176">Die folgenden Werte in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beide aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1aa71-176">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="1aa71-177">**SE \_ DACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="1aa71-177">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="1aa71-178">Gibt an, dass die DACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aa71-178">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="1aa71-179">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.</span><span class="sxs-lookup"><span data-stu-id="1aa71-179">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="1aa71-180">**SE \_ SACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="1aa71-180">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="1aa71-181">Gibt an, dass die SACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aa71-181">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="1aa71-182">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei.</span><span class="sxs-lookup"><span data-stu-id="1aa71-182">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="1aa71-183">Zum Aktualisieren der SACL muss für das Konto die **SeSecurityPrivilege-Berechtigung** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="1aa71-183">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="1aa71-184">Für die Skripterstellung lautet der Berechtigungsname **SeSecurityPrivilege.**</span><span class="sxs-lookup"><span data-stu-id="1aa71-184">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="1aa71-185">Weitere Informationen finden Sie unter [**Berechtigungskonstanten.**](/windows/desktop/WmiSdk/privilege-constants)</span><span class="sxs-lookup"><span data-stu-id="1aa71-185">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="1aa71-186">Wenn der Gruppentreuhänder und die Eigenschaften des Besitzertreuhänders nicht **NULL sind,** werden sie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1aa71-186">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="1aa71-187">Andernfalls behält WMI die ursprünglichen Werte bei.</span><span class="sxs-lookup"><span data-stu-id="1aa71-187">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="1aa71-188">Weitere Informationen finden Sie unter [WMI-Sicherheitsdeskriptorobjekte.](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)</span><span class="sxs-lookup"><span data-stu-id="1aa71-188">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="1aa71-189">Wenn eine neue SACL in einem Aufruf dieser Methode **NULL** ist, bleibt die Sicherheitsbeschreibung SACL für das sicherungsfähige Zielobjekt unverändert.</span><span class="sxs-lookup"><span data-stu-id="1aa71-189">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa71-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aa71-190">Requirements</span></span>



| <span data-ttu-id="1aa71-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aa71-191">Requirement</span></span> | <span data-ttu-id="1aa71-192">Wert</span><span class="sxs-lookup"><span data-stu-id="1aa71-192">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa71-193">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1aa71-193">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa71-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1aa71-194">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1aa71-195">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1aa71-195">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa71-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aa71-196">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1aa71-197">Namespace</span><span class="sxs-lookup"><span data-stu-id="1aa71-197">Namespace</span></span><br/>                | <span data-ttu-id="1aa71-198">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="1aa71-198">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1aa71-199">MOF</span><span class="sxs-lookup"><span data-stu-id="1aa71-199">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aa71-200"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aa71-200"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aa71-201">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa71-201">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aa71-202"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa71-202"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa71-203">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1aa71-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa71-204">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="1aa71-204">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="1aa71-205">**Berechtigungskonst constants**</span><span class="sxs-lookup"><span data-stu-id="1aa71-205">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="1aa71-206">WMI-Sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="1aa71-206">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="1aa71-207">Ändern der Zugriffssicherheit für sicherungsfähige Objekte</span><span class="sxs-lookup"><span data-stu-id="1aa71-207">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="1aa71-208">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="1aa71-208">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

