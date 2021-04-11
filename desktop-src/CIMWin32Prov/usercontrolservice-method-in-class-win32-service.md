---
description: Versucht, einen benutzerdefinierten Steuerelement Code an den Dienst zu senden, auf den verwiesen wird.
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: UserControlService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8c523617826bd5d608b8c6b1ee242863f7591a61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958550"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c974a-103">UserControlService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="c974a-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c974a-104">Die **UserControlService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, einen benutzerdefinierten Steuerelement Code an den Dienst zu senden, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c974a-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="c974a-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c974a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c974a-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c974a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c974a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c974a-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="c974a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c974a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c974a-109">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c974a-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c974a-110">Gibt definierte Werte an (von 128 bis 255), die für einen benutzerspezifische Steuerungsbefehle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c974a-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c974a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c974a-111">Return value</span></span>

<span data-ttu-id="c974a-112">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c974a-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c974a-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c974a-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c974a-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c974a-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c974a-115">**0**</span><span class="sxs-lookup"><span data-stu-id="c974a-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-116">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c974a-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-117">**1**</span><span class="sxs-lookup"><span data-stu-id="c974a-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-118">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c974a-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-119">**2**</span><span class="sxs-lookup"><span data-stu-id="c974a-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-120">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c974a-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-121">**3**</span><span class="sxs-lookup"><span data-stu-id="c974a-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-122">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c974a-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-123">**4**</span><span class="sxs-lookup"><span data-stu-id="c974a-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-124">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="c974a-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-125">**5**</span><span class="sxs-lookup"><span data-stu-id="c974a-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-126">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="c974a-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-127">**6**</span><span class="sxs-lookup"><span data-stu-id="c974a-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-128">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c974a-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-129">**7**</span><span class="sxs-lookup"><span data-stu-id="c974a-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-130">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="c974a-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-131">**8**</span><span class="sxs-lookup"><span data-stu-id="c974a-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-132">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c974a-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-133">**9**</span><span class="sxs-lookup"><span data-stu-id="c974a-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-134">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c974a-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-135">**10**</span><span class="sxs-lookup"><span data-stu-id="c974a-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-136">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c974a-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-137">**11**</span><span class="sxs-lookup"><span data-stu-id="c974a-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-138">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c974a-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-139">**12**</span><span class="sxs-lookup"><span data-stu-id="c974a-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-140">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c974a-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-141">**13**</span><span class="sxs-lookup"><span data-stu-id="c974a-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-142">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c974a-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-143">**14**</span><span class="sxs-lookup"><span data-stu-id="c974a-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-144">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c974a-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-145">**15**</span><span class="sxs-lookup"><span data-stu-id="c974a-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-146">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c974a-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-147">**16**</span><span class="sxs-lookup"><span data-stu-id="c974a-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-148">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c974a-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-149">**17**</span><span class="sxs-lookup"><span data-stu-id="c974a-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-150">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="c974a-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-151">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="c974a-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-152">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c974a-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-153">**19**</span><span class="sxs-lookup"><span data-stu-id="c974a-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-154">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c974a-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-155">**20**</span><span class="sxs-lookup"><span data-stu-id="c974a-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-156">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c974a-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-157">**21**</span><span class="sxs-lookup"><span data-stu-id="c974a-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-158">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c974a-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-159">**22**</span><span class="sxs-lookup"><span data-stu-id="c974a-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-160">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c974a-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-161">**23**</span><span class="sxs-lookup"><span data-stu-id="c974a-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-162">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c974a-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c974a-163">**24**</span><span class="sxs-lookup"><span data-stu-id="c974a-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c974a-164">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="c974a-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c974a-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c974a-165">Requirements</span></span>



| <span data-ttu-id="c974a-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c974a-166">Requirement</span></span> | <span data-ttu-id="c974a-167">Wert</span><span class="sxs-lookup"><span data-stu-id="c974a-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c974a-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c974a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c974a-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c974a-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c974a-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c974a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c974a-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c974a-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c974a-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="c974a-172">Namespace</span></span><br/>                | <span data-ttu-id="c974a-173">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c974a-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c974a-174">MOF</span><span class="sxs-lookup"><span data-stu-id="c974a-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c974a-175"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c974a-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c974a-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c974a-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c974a-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c974a-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c974a-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c974a-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="c974a-179">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c974a-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c974a-180">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c974a-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

