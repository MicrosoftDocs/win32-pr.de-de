---
title: UserControlService-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Versucht, einen benutzerdefinierten Steuerelement Code an den Dienst zu senden, auf den verwiesen wird.
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- UserControlService-Methode Remotedesktopdienste
- UserControlService-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, UserControlService-Methode
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
ms.openlocfilehash: 15b1ea4f5e82814aad7549085070b0583993024b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478846"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="ab893-106">UserControlService-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="ab893-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="ab893-107">Die **UserControlService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, einen benutzerdefinierten Steuerelement Code an den Dienst zu senden, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ab893-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="ab893-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab893-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ab893-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ab893-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab893-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab893-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="ab893-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab893-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab893-112">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab893-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab893-113">Gibt definierte Werte an (von 128 bis 255), die für einen benutzerspezifische Steuerungsbefehle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ab893-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab893-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab893-114">Return value</span></span>

<span data-ttu-id="ab893-115">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ab893-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ab893-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ab893-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ab893-117">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ab893-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ab893-118">**0**</span><span class="sxs-lookup"><span data-stu-id="ab893-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-119">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="ab893-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-120">**1**</span><span class="sxs-lookup"><span data-stu-id="ab893-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-121">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab893-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-122">**2**</span><span class="sxs-lookup"><span data-stu-id="ab893-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-123">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="ab893-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-124">**3**</span><span class="sxs-lookup"><span data-stu-id="ab893-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-125">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ab893-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-126">**4**</span><span class="sxs-lookup"><span data-stu-id="ab893-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-127">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="ab893-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-128">**5**</span><span class="sxs-lookup"><span data-stu-id="ab893-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-129">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="ab893-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-130">**6**</span><span class="sxs-lookup"><span data-stu-id="ab893-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-131">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="ab893-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-132">**7**</span><span class="sxs-lookup"><span data-stu-id="ab893-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-133">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="ab893-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-134">**8**</span><span class="sxs-lookup"><span data-stu-id="ab893-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-135">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ab893-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-136">**9**</span><span class="sxs-lookup"><span data-stu-id="ab893-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-137">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ab893-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-138">**10**</span><span class="sxs-lookup"><span data-stu-id="ab893-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-139">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab893-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-140">**11**</span><span class="sxs-lookup"><span data-stu-id="ab893-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-141">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="ab893-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-142">**12**</span><span class="sxs-lookup"><span data-stu-id="ab893-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-143">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ab893-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-144">**13**</span><span class="sxs-lookup"><span data-stu-id="ab893-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-145">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ab893-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-146">**14**</span><span class="sxs-lookup"><span data-stu-id="ab893-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-147">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab893-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-148">**15**</span><span class="sxs-lookup"><span data-stu-id="ab893-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-149">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ab893-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-150">**16**</span><span class="sxs-lookup"><span data-stu-id="ab893-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-151">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ab893-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-152">**17**</span><span class="sxs-lookup"><span data-stu-id="ab893-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-153">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="ab893-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-154">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="ab893-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-155">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ab893-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-156">**19**</span><span class="sxs-lookup"><span data-stu-id="ab893-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-157">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab893-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-158">**20**</span><span class="sxs-lookup"><span data-stu-id="ab893-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-159">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ab893-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-160">**21**</span><span class="sxs-lookup"><span data-stu-id="ab893-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-161">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ab893-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-162">**22**</span><span class="sxs-lookup"><span data-stu-id="ab893-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-163">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ab893-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-164">**23**</span><span class="sxs-lookup"><span data-stu-id="ab893-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-165">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ab893-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab893-166">**24**</span><span class="sxs-lookup"><span data-stu-id="ab893-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ab893-167">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="ab893-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab893-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab893-168">Requirements</span></span>



| <span data-ttu-id="ab893-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab893-169">Requirement</span></span> | <span data-ttu-id="ab893-170">Wert</span><span class="sxs-lookup"><span data-stu-id="ab893-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab893-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab893-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ab893-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab893-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab893-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab893-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ab893-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab893-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab893-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab893-175">Namespace</span></span><br/>                | <span data-ttu-id="ab893-176">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ab893-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ab893-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ab893-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab893-178"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab893-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab893-179">DLL</span><span class="sxs-lookup"><span data-stu-id="ab893-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab893-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab893-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab893-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab893-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab893-182">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="ab893-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="ab893-183">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="ab893-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="ab893-184">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="ab893-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

