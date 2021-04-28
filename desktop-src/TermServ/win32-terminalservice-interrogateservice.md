---
title: InterrogateService-Methode der Win32_Service -Klasse (Remotedesktopdienste)
description: 'InterrogateService-Methode der Win32_Service -Klasse (Remotedesktopdienste): Fordert an, dass der Dienst, auf den verwiesen wird, seinen Zustand an den Service Manager aktualisiert.'
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- InterrogateService-Remotedesktopdienste
- InterrogateService-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service klasse Remotedesktopdienste , InterrogateService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850953b210ea11b9dd1000326d6793e3651ce538
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090658"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="1e10a-106">InterrogateService-Methode der Win32_Service -Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="1e10a-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="1e10a-107">Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** fordert an, dass der Dienst, auf den verwiesen wird, seinen Zustand auf den Dienst-Manager aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1e10a-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="1e10a-108">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e10a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1e10a-109">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="1e10a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e10a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e10a-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="1e10a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e10a-111">Parameters</span></span>

<span data-ttu-id="1e10a-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e10a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e10a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e10a-113">Return value</span></span>

<span data-ttu-id="1e10a-114">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um auf einen Fehler hindeuten zu können.</span><span class="sxs-lookup"><span data-stu-id="1e10a-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="1e10a-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1e10a-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1e10a-116">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1e10a-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1e10a-117">**0**</span><span class="sxs-lookup"><span data-stu-id="1e10a-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-118">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1e10a-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-119">**1**</span><span class="sxs-lookup"><span data-stu-id="1e10a-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-120">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e10a-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-121">**2**</span><span class="sxs-lookup"><span data-stu-id="1e10a-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-122">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="1e10a-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-123">**3**</span><span class="sxs-lookup"><span data-stu-id="1e10a-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-124">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="1e10a-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-125">**4**</span><span class="sxs-lookup"><span data-stu-id="1e10a-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="1e10a-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-127">**5**</span><span class="sxs-lookup"><span data-stu-id="1e10a-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-128">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="1e10a-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-129">**6**</span><span class="sxs-lookup"><span data-stu-id="1e10a-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-130">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="1e10a-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-131">**7**</span><span class="sxs-lookup"><span data-stu-id="1e10a-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-132">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="1e10a-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-133">**8**</span><span class="sxs-lookup"><span data-stu-id="1e10a-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-134">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1e10a-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-135">**9**</span><span class="sxs-lookup"><span data-stu-id="1e10a-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-136">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1e10a-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-137">**10**</span><span class="sxs-lookup"><span data-stu-id="1e10a-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e10a-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-139">**11**</span><span class="sxs-lookup"><span data-stu-id="1e10a-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1e10a-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-141">**12**</span><span class="sxs-lookup"><span data-stu-id="1e10a-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-142">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e10a-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-143">**13**</span><span class="sxs-lookup"><span data-stu-id="1e10a-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1e10a-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-145">**14**</span><span class="sxs-lookup"><span data-stu-id="1e10a-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1e10a-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-147">**15**</span><span class="sxs-lookup"><span data-stu-id="1e10a-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1e10a-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-149">**16**</span><span class="sxs-lookup"><span data-stu-id="1e10a-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e10a-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-151">**17**</span><span class="sxs-lookup"><span data-stu-id="1e10a-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-152">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="1e10a-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-153">**18**</span><span class="sxs-lookup"><span data-stu-id="1e10a-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-154">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="1e10a-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-155">**19**</span><span class="sxs-lookup"><span data-stu-id="1e10a-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-156">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e10a-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-157">**20**</span><span class="sxs-lookup"><span data-stu-id="1e10a-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-158">Der Dienstname weist ungültige Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="1e10a-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-159">**21**</span><span class="sxs-lookup"><span data-stu-id="1e10a-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-160">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="1e10a-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-161">**22**</span><span class="sxs-lookup"><span data-stu-id="1e10a-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-162">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1e10a-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-163">**23**</span><span class="sxs-lookup"><span data-stu-id="1e10a-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-164">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1e10a-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e10a-165">**24**</span><span class="sxs-lookup"><span data-stu-id="1e10a-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="1e10a-166">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="1e10a-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e10a-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e10a-167">Requirements</span></span>



| <span data-ttu-id="1e10a-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e10a-168">Requirement</span></span> | <span data-ttu-id="1e10a-169">Wert</span><span class="sxs-lookup"><span data-stu-id="1e10a-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e10a-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e10a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1e10a-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e10a-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e10a-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e10a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1e10a-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e10a-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e10a-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e10a-174">Namespace</span></span><br/>                | <span data-ttu-id="1e10a-175">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1e10a-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e10a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="1e10a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e10a-177"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e10a-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e10a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="1e10a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e10a-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e10a-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e10a-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e10a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e10a-181">**\_Win32-Dienst**</span><span class="sxs-lookup"><span data-stu-id="1e10a-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="1e10a-182">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="1e10a-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="1e10a-183">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="1e10a-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="1e10a-184">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="1e10a-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

