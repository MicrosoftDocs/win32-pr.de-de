---
description: Versucht, den Dienst anzuhalten.
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: PauseService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b1dfa0b956442f74c17dd6a8c054c229a92466a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342746"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="25262-103">PauseService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="25262-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="25262-104">Die " **PauseService** "- [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, den Dienst im angehaltenen Zustand zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="25262-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="25262-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="25262-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="25262-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="25262-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="25262-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="25262-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="25262-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="25262-108">Parameters</span></span>

<span data-ttu-id="25262-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="25262-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25262-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25262-110">Return value</span></span>

<span data-ttu-id="25262-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="25262-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="25262-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="25262-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="25262-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="25262-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="25262-114">**0**</span><span class="sxs-lookup"><span data-stu-id="25262-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="25262-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="25262-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="25262-116">**1**</span><span class="sxs-lookup"><span data-stu-id="25262-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="25262-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25262-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="25262-118">**2**</span><span class="sxs-lookup"><span data-stu-id="25262-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="25262-119">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="25262-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="25262-120">**3**</span><span class="sxs-lookup"><span data-stu-id="25262-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="25262-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="25262-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="25262-122">**4**</span><span class="sxs-lookup"><span data-stu-id="25262-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="25262-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="25262-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="25262-124">**5**</span><span class="sxs-lookup"><span data-stu-id="25262-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="25262-125">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="25262-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="25262-126">**6**</span><span class="sxs-lookup"><span data-stu-id="25262-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="25262-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="25262-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="25262-128">**7**</span><span class="sxs-lookup"><span data-stu-id="25262-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="25262-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="25262-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="25262-130">**8**</span><span class="sxs-lookup"><span data-stu-id="25262-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="25262-131">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="25262-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="25262-132">**9**</span><span class="sxs-lookup"><span data-stu-id="25262-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="25262-133">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="25262-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="25262-134">**10**</span><span class="sxs-lookup"><span data-stu-id="25262-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="25262-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25262-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="25262-136">**11**</span><span class="sxs-lookup"><span data-stu-id="25262-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="25262-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="25262-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="25262-138">**12**</span><span class="sxs-lookup"><span data-stu-id="25262-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="25262-139">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="25262-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="25262-140">**13**</span><span class="sxs-lookup"><span data-stu-id="25262-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="25262-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="25262-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="25262-142">**14**</span><span class="sxs-lookup"><span data-stu-id="25262-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="25262-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="25262-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="25262-144">**15**</span><span class="sxs-lookup"><span data-stu-id="25262-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="25262-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="25262-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="25262-146">**16**</span><span class="sxs-lookup"><span data-stu-id="25262-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="25262-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="25262-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="25262-148">**17**</span><span class="sxs-lookup"><span data-stu-id="25262-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="25262-149">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="25262-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="25262-150">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="25262-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="25262-151">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="25262-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="25262-152">**19**</span><span class="sxs-lookup"><span data-stu-id="25262-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="25262-153">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25262-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="25262-154">**20**</span><span class="sxs-lookup"><span data-stu-id="25262-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="25262-155">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="25262-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="25262-156">**21**</span><span class="sxs-lookup"><span data-stu-id="25262-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="25262-157">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="25262-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="25262-158">**22**</span><span class="sxs-lookup"><span data-stu-id="25262-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="25262-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="25262-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="25262-160">**23**</span><span class="sxs-lookup"><span data-stu-id="25262-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="25262-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="25262-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="25262-162">**24**</span><span class="sxs-lookup"><span data-stu-id="25262-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="25262-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="25262-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25262-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25262-164">Remarks</span></span>

<span data-ttu-id="25262-165">Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die-Methode [**StopService**](stopservice-method-in-class-win32-service.md) und die [**anhaleservice**](pauseservice-method-in-class-win32-systemdriver.md) -Methode verwenden, um-Dienste anzuhalten und anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="25262-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="25262-166">Die Entscheidung, einen Dienst zu stoppen, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="25262-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="25262-167">Ist der Dienst in der Lage, angehalten zu werden?</span><span class="sxs-lookup"><span data-stu-id="25262-167">Is the service capable of being paused?</span></span> <span data-ttu-id="25262-168">Wenn dies nicht der Wert ist, ist die einzige Option der Dienst wird beendet.</span><span class="sxs-lookup"><span data-stu-id="25262-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="25262-169">Müssen Sie die Verarbeitung von Client Anforderungen für alle Benutzer fortsetzen, die bereits mit dem Dienst verbunden sind?</span><span class="sxs-lookup"><span data-stu-id="25262-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="25262-170">Wenn dies der Fall ist, ermöglicht das Anhalten eines Dienstanbieter in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert</span><span class="sxs-lookup"><span data-stu-id="25262-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="25262-171">Wenn Sie einen Dienst beenden, werden dagegen alle Clients sofort getrennt.</span><span class="sxs-lookup"><span data-stu-id="25262-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="25262-172">Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden?</span><span class="sxs-lookup"><span data-stu-id="25262-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="25262-173">Obwohl Dienst Eigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten nicht wirksam, bis der Dienst tatsächlich beendet und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="25262-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="25262-174">Der zum Anhalten eines Dienstanbieter erforderliche Skriptcode ist nahezu identisch mit dem Code, der zum Anhalten des Dienstanbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="25262-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="25262-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25262-175">Examples</span></span>

<span data-ttu-id="25262-176">Die [Unterbrechungs Dienste, die unter einem bestimmten](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript-Konto ausgeführt werden, halten alle Dienste an, die unter dem hypothetischen Dienst Konto "netzvc" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="25262-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="25262-177">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32- \_ Dienstanbieter**](win32-service.md)angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="25262-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="25262-178">Der Dienst muss angehalten und bereits ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="25262-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="25262-179">Im folgenden perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32- \_ Dienstanbieter**](win32-service.md)angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="25262-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="25262-180">Der Dienst muss angehalten und bereits ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="25262-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="25262-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25262-181">Requirements</span></span>



| <span data-ttu-id="25262-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25262-182">Requirement</span></span> | <span data-ttu-id="25262-183">Wert</span><span class="sxs-lookup"><span data-stu-id="25262-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25262-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25262-184">Minimum supported client</span></span><br/> | <span data-ttu-id="25262-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25262-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25262-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25262-186">Minimum supported server</span></span><br/> | <span data-ttu-id="25262-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25262-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25262-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="25262-188">Namespace</span></span><br/>                | <span data-ttu-id="25262-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="25262-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="25262-190">MOF</span><span class="sxs-lookup"><span data-stu-id="25262-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25262-191"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="25262-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25262-192">DLL</span><span class="sxs-lookup"><span data-stu-id="25262-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25262-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25262-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25262-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25262-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="25262-195">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="25262-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="25262-196">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="25262-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="25262-197">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="25262-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="25262-198">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="25262-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

