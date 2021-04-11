---
description: Fordert an, dass der Dienst, auf den verwiesen wird, seinen Status an Service Manager aktualisiert.
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: InterrogateService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ad1f56afcbe42ced19da823c454291a7b5282d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126476"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="8c0b4-103">InterrogateService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="8c0b4-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8c0b4-104">Die Methode " **InterrogateService** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " fordert an, dass der Dienst, auf den verwiesen wird, seinen Status an den Dienst Manager</span><span class="sxs-lookup"><span data-stu-id="8c0b4-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="8c0b4-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8c0b4-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8c0b4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c0b4-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="8c0b4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c0b4-108">Parameters</span></span>

<span data-ttu-id="8c0b4-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c0b4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c0b4-110">Return value</span></span>

<span data-ttu-id="8c0b4-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="8c0b4-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8c0b4-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8c0b4-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8c0b4-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8c0b4-114">**0**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-116">**1**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-118">**2**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-119">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-120">**3**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-122">**4**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-124">**5**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-125">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-126">**6**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-128">**7**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-130">**8**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-131">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-132">**9**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-133">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-134">**10**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-136">**11**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-138">**12**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-139">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-140">**13**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-142">**14**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-144">**15**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-146">**16**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-148">**17**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-149">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-150">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-151">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-152">**19**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-153">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-154">**20**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-155">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-156">**21**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-157">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-158">**22**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-160">**23**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8c0b4-162">**24**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="8c0b4-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="8c0b4-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c0b4-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c0b4-164">Requirements</span></span>



| <span data-ttu-id="8c0b4-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c0b4-165">Requirement</span></span> | <span data-ttu-id="8c0b4-166">Wert</span><span class="sxs-lookup"><span data-stu-id="8c0b4-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0b4-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c0b4-167">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0b4-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c0b4-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c0b4-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c0b4-169">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0b4-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c0b4-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c0b4-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c0b4-171">Namespace</span></span><br/>                | <span data-ttu-id="8c0b4-172">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c0b4-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c0b4-173">MOF</span><span class="sxs-lookup"><span data-stu-id="8c0b4-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c0b4-174"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8c0b4-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c0b4-175">DLL</span><span class="sxs-lookup"><span data-stu-id="8c0b4-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c0b4-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c0b4-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0b4-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c0b4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0b4-178">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="8c0b4-179">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c0b4-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8c0b4-180">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="8c0b4-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="8c0b4-181">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="8c0b4-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

