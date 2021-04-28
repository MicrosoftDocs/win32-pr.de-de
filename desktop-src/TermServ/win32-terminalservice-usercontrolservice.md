---
title: UserControlService-Methode der Win32_Service -Klasse (Remotedesktopdienste)
description: 'UserControlService-Methode der Win32_Service -Klasse (Remotedesktopdienste): Versucht, einen benutzerdefinierten Steuerelementcode an den Dienst zu senden, auf den verwiesen wird.'
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- UserControlService-Remotedesktopdienste
- UserControlService-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service klasse Remotedesktopdienste , UserControlService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71a33056f596afaf577968a5c725b3f64f79b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090608"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="41ca4-106">UserControlService-Methode der Win32_Service -Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="41ca4-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="41ca4-107">Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** versucht, einen benutzerdefinierten Steuerelementcode an den Dienst zu senden, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="41ca4-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="41ca4-108">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="41ca4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41ca4-109">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="41ca4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41ca4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="41ca4-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="41ca4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="41ca4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ca4-112">*ControlCode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="41ca4-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-113">Gibt definierte Werte (von 128 bis 255) an, die für einen Benutzer spezifische Steuerungsbefehle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="41ca4-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ca4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41ca4-114">Return value</span></span>

<span data-ttu-id="41ca4-115">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41ca4-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="41ca4-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="41ca4-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="41ca4-117">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="41ca4-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="41ca4-118">**0**</span><span class="sxs-lookup"><span data-stu-id="41ca4-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-119">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="41ca4-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-120">**1**</span><span class="sxs-lookup"><span data-stu-id="41ca4-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-121">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41ca4-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-122">**2**</span><span class="sxs-lookup"><span data-stu-id="41ca4-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-123">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="41ca4-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-124">**3**</span><span class="sxs-lookup"><span data-stu-id="41ca4-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-125">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="41ca4-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-126">**4**</span><span class="sxs-lookup"><span data-stu-id="41ca4-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-127">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="41ca4-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-128">**5**</span><span class="sxs-lookup"><span data-stu-id="41ca4-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-129">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="41ca4-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-130">**6**</span><span class="sxs-lookup"><span data-stu-id="41ca4-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-131">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="41ca4-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-132">**7**</span><span class="sxs-lookup"><span data-stu-id="41ca4-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-133">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="41ca4-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-134">**8**</span><span class="sxs-lookup"><span data-stu-id="41ca4-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-135">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="41ca4-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-136">**9**</span><span class="sxs-lookup"><span data-stu-id="41ca4-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-137">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="41ca4-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-138">**10**</span><span class="sxs-lookup"><span data-stu-id="41ca4-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-139">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41ca4-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-140">**11**</span><span class="sxs-lookup"><span data-stu-id="41ca4-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-141">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="41ca4-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-142">**12**</span><span class="sxs-lookup"><span data-stu-id="41ca4-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-143">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="41ca4-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-144">**13**</span><span class="sxs-lookup"><span data-stu-id="41ca4-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-145">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="41ca4-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-146">**14**</span><span class="sxs-lookup"><span data-stu-id="41ca4-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-147">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="41ca4-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-148">**15**</span><span class="sxs-lookup"><span data-stu-id="41ca4-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-149">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="41ca4-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-150">**16**</span><span class="sxs-lookup"><span data-stu-id="41ca4-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-151">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="41ca4-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-152">**17**</span><span class="sxs-lookup"><span data-stu-id="41ca4-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-153">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="41ca4-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-154">**18**</span><span class="sxs-lookup"><span data-stu-id="41ca4-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-155">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="41ca4-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-156">**19**</span><span class="sxs-lookup"><span data-stu-id="41ca4-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-157">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41ca4-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-158">**20**</span><span class="sxs-lookup"><span data-stu-id="41ca4-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-159">Der Dienstname weist ungültige Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="41ca4-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-160">**21**</span><span class="sxs-lookup"><span data-stu-id="41ca4-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-161">An den Dienst wurden ungültige Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="41ca4-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-162">**22**</span><span class="sxs-lookup"><span data-stu-id="41ca4-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-163">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="41ca4-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-164">**23**</span><span class="sxs-lookup"><span data-stu-id="41ca4-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-165">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41ca4-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41ca4-166">**24**</span><span class="sxs-lookup"><span data-stu-id="41ca4-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="41ca4-167">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="41ca4-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41ca4-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41ca4-168">Requirements</span></span>



| <span data-ttu-id="41ca4-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41ca4-169">Requirement</span></span> | <span data-ttu-id="41ca4-170">Wert</span><span class="sxs-lookup"><span data-stu-id="41ca4-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41ca4-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41ca4-171">Minimum supported client</span></span><br/> | <span data-ttu-id="41ca4-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41ca4-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41ca4-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41ca4-173">Minimum supported server</span></span><br/> | <span data-ttu-id="41ca4-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41ca4-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41ca4-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="41ca4-175">Namespace</span></span><br/>                | <span data-ttu-id="41ca4-176">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="41ca4-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="41ca4-177">MOF</span><span class="sxs-lookup"><span data-stu-id="41ca4-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41ca4-178"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="41ca4-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="41ca4-179">DLL</span><span class="sxs-lookup"><span data-stu-id="41ca4-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41ca4-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41ca4-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41ca4-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="41ca4-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ca4-182">**\_Win32-Dienst**</span><span class="sxs-lookup"><span data-stu-id="41ca4-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="41ca4-183">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="41ca4-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="41ca4-184">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="41ca4-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

