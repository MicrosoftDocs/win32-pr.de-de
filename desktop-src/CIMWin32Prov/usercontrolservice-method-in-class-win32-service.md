---
description: 'UserControlService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter): Versucht, einen benutzerdefinierten Steuerelementcode an den Dienst zu senden, auf den verwiesen wird.'
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: UserControlService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)
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
ms.openlocfilehash: 455128b35c2645c6aa6ea10f64d12dff392fecca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100001"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="15907-103">UserControlService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="15907-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="15907-104">Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** versucht, einen benutzerdefinierten Steuerelementcode an den Dienst zu senden, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="15907-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="15907-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="15907-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="15907-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="15907-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="15907-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="15907-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="15907-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15907-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15907-109">*ControlCode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="15907-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15907-110">Gibt definierte Werte (von 128 bis 255) an, die für einen Benutzer spezifische Steuerungsbefehle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="15907-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15907-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15907-111">Return value</span></span>

<span data-ttu-id="15907-112">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="15907-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="15907-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="15907-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="15907-114">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="15907-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="15907-115">**0**</span><span class="sxs-lookup"><span data-stu-id="15907-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="15907-116">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="15907-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="15907-117">**1**</span><span class="sxs-lookup"><span data-stu-id="15907-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="15907-118">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15907-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="15907-119">**2**</span><span class="sxs-lookup"><span data-stu-id="15907-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="15907-120">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="15907-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="15907-121">**3**</span><span class="sxs-lookup"><span data-stu-id="15907-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="15907-122">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="15907-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="15907-123">**4**</span><span class="sxs-lookup"><span data-stu-id="15907-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="15907-124">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="15907-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="15907-125">**5**</span><span class="sxs-lookup"><span data-stu-id="15907-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="15907-126">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="15907-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="15907-127">**6**</span><span class="sxs-lookup"><span data-stu-id="15907-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="15907-128">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="15907-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="15907-129">**7**</span><span class="sxs-lookup"><span data-stu-id="15907-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="15907-130">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="15907-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="15907-131">**8**</span><span class="sxs-lookup"><span data-stu-id="15907-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="15907-132">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="15907-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="15907-133">**9**</span><span class="sxs-lookup"><span data-stu-id="15907-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="15907-134">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="15907-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="15907-135">**10**</span><span class="sxs-lookup"><span data-stu-id="15907-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="15907-136">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15907-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="15907-137">**11**</span><span class="sxs-lookup"><span data-stu-id="15907-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="15907-138">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="15907-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="15907-139">**12**</span><span class="sxs-lookup"><span data-stu-id="15907-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="15907-140">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="15907-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15907-141">**13**</span><span class="sxs-lookup"><span data-stu-id="15907-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="15907-142">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="15907-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="15907-143">**14**</span><span class="sxs-lookup"><span data-stu-id="15907-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="15907-144">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="15907-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15907-145">**15**</span><span class="sxs-lookup"><span data-stu-id="15907-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="15907-146">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="15907-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="15907-147">**16**</span><span class="sxs-lookup"><span data-stu-id="15907-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="15907-148">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="15907-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15907-149">**17**</span><span class="sxs-lookup"><span data-stu-id="15907-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="15907-150">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="15907-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="15907-151">**18**</span><span class="sxs-lookup"><span data-stu-id="15907-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="15907-152">Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="15907-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="15907-153">**19**</span><span class="sxs-lookup"><span data-stu-id="15907-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="15907-154">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15907-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="15907-155">**20**</span><span class="sxs-lookup"><span data-stu-id="15907-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="15907-156">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="15907-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="15907-157">**21**</span><span class="sxs-lookup"><span data-stu-id="15907-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="15907-158">An den Dienst wurden ungültige Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="15907-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="15907-159">**22**</span><span class="sxs-lookup"><span data-stu-id="15907-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="15907-160">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="15907-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="15907-161">**23**</span><span class="sxs-lookup"><span data-stu-id="15907-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="15907-162">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="15907-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15907-163">**24**</span><span class="sxs-lookup"><span data-stu-id="15907-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="15907-164">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="15907-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15907-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15907-165">Requirements</span></span>



| <span data-ttu-id="15907-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15907-166">Requirement</span></span> | <span data-ttu-id="15907-167">Wert</span><span class="sxs-lookup"><span data-stu-id="15907-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15907-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15907-168">Minimum supported client</span></span><br/> | <span data-ttu-id="15907-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15907-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15907-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15907-170">Minimum supported server</span></span><br/> | <span data-ttu-id="15907-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15907-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15907-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="15907-172">Namespace</span></span><br/>                | <span data-ttu-id="15907-173">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15907-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15907-174">MOF</span><span class="sxs-lookup"><span data-stu-id="15907-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15907-175"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="15907-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15907-176">DLL</span><span class="sxs-lookup"><span data-stu-id="15907-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15907-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15907-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15907-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15907-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="15907-179">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15907-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="15907-180">**\_Win32-Dienst**</span><span class="sxs-lookup"><span data-stu-id="15907-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

