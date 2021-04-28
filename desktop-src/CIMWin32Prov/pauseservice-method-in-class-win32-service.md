---
description: 'PauseService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter): Versucht, den Dienst im angehaltenen Zustand zu platzieren.'
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: PauseService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)
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
ms.openlocfilehash: 7654feea410564137e98861c4c0b5de2b5e7192e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096948"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="2421c-103">PauseService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="2421c-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="2421c-104">Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** versucht, den Dienst im angehaltenen Zustand zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="2421c-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="2421c-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2421c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2421c-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="2421c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2421c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2421c-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="2421c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2421c-108">Parameters</span></span>

<span data-ttu-id="2421c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2421c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2421c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2421c-110">Return value</span></span>

<span data-ttu-id="2421c-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2421c-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="2421c-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2421c-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2421c-113">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2421c-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2421c-114">**0**</span><span class="sxs-lookup"><span data-stu-id="2421c-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2421c-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-116">**1**</span><span class="sxs-lookup"><span data-stu-id="2421c-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2421c-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-118">**2**</span><span class="sxs-lookup"><span data-stu-id="2421c-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-119">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="2421c-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-120">**3**</span><span class="sxs-lookup"><span data-stu-id="2421c-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="2421c-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-122">**4**</span><span class="sxs-lookup"><span data-stu-id="2421c-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="2421c-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-124">**5**</span><span class="sxs-lookup"><span data-stu-id="2421c-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-125">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="2421c-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-126">**6**</span><span class="sxs-lookup"><span data-stu-id="2421c-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="2421c-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-128">**7**</span><span class="sxs-lookup"><span data-stu-id="2421c-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="2421c-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-130">**8**</span><span class="sxs-lookup"><span data-stu-id="2421c-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-131">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="2421c-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-132">**9**</span><span class="sxs-lookup"><span data-stu-id="2421c-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-133">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="2421c-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-134">**10**</span><span class="sxs-lookup"><span data-stu-id="2421c-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2421c-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-136">**11**</span><span class="sxs-lookup"><span data-stu-id="2421c-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2421c-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-138">**12**</span><span class="sxs-lookup"><span data-stu-id="2421c-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-139">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="2421c-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-140">**13**</span><span class="sxs-lookup"><span data-stu-id="2421c-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2421c-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-142">**14**</span><span class="sxs-lookup"><span data-stu-id="2421c-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2421c-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-144">**15**</span><span class="sxs-lookup"><span data-stu-id="2421c-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="2421c-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-146">**16**</span><span class="sxs-lookup"><span data-stu-id="2421c-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="2421c-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-148">**17**</span><span class="sxs-lookup"><span data-stu-id="2421c-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-149">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="2421c-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-150">**18**</span><span class="sxs-lookup"><span data-stu-id="2421c-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-151">Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="2421c-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-152">**19**</span><span class="sxs-lookup"><span data-stu-id="2421c-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-153">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2421c-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-154">**20**</span><span class="sxs-lookup"><span data-stu-id="2421c-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-155">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2421c-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-156">**21**</span><span class="sxs-lookup"><span data-stu-id="2421c-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-157">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="2421c-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-158">**22**</span><span class="sxs-lookup"><span data-stu-id="2421c-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="2421c-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-160">**23**</span><span class="sxs-lookup"><span data-stu-id="2421c-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2421c-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2421c-162">**24**</span><span class="sxs-lookup"><span data-stu-id="2421c-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="2421c-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="2421c-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2421c-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2421c-164">Remarks</span></span>

<span data-ttu-id="2421c-165">Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die Dienste mithilfe der Methoden [**StopService**](stopservice-method-in-class-win32-service.md) und [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) beenden und anhalten.</span><span class="sxs-lookup"><span data-stu-id="2421c-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="2421c-166">Die Entscheidung, einen Dienst anzuhalten, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="2421c-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="2421c-167">Kann der Dienst angehalten werden?</span><span class="sxs-lookup"><span data-stu-id="2421c-167">Is the service capable of being paused?</span></span> <span data-ttu-id="2421c-168">Wenn dies nicht dere ist, ist die einzige Option das Beenden des Diensts.</span><span class="sxs-lookup"><span data-stu-id="2421c-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="2421c-169">Müssen Sie weiterhin Clientanforderungen für personen verarbeiten, die bereits mit dem Dienst verbunden sind?</span><span class="sxs-lookup"><span data-stu-id="2421c-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="2421c-170">In diesem Falle ermöglicht das Anhalten eines Diensts in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="2421c-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="2421c-171">Wenn Sie dagegen einen Dienst beenden, werden alle Clients sofort getrennt.</span><span class="sxs-lookup"><span data-stu-id="2421c-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="2421c-172">Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden?</span><span class="sxs-lookup"><span data-stu-id="2421c-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="2421c-173">Obwohl Diensteigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten erst wirksam, wenn der Dienst tatsächlich beendet und neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="2421c-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="2421c-174">Der Skriptcode, der zum Beenden eines Diensts erforderlich ist, ist fast identisch mit dem Code, der zum Anhalten des Diensts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2421c-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="2421c-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2421c-175">Examples</span></span>

<span data-ttu-id="2421c-176">Im VBScript-Beispiel Dienste anhalten, die [unter einem bestimmten Konto ausgeführt werden,](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) werden alle Dienste angehalten, die unter dem hypothetischen Dienstkonto "Netsvc" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2421c-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="2421c-177">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**\_ Win32-Diensts**](win32-service.md)angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2421c-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="2421c-178">Der Dienst muss das Anhalten unterstützen und bereits ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2421c-178">The service must support pausing and be running already.</span></span>

 


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



<span data-ttu-id="2421c-179">Im folgenden Perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**\_ Win32-Diensts**](win32-service.md)angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2421c-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="2421c-180">Der Dienst muss das Anhalten unterstützen und bereits ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2421c-180">The service must support pausing and be running already.</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="2421c-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2421c-181">Requirements</span></span>



| <span data-ttu-id="2421c-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2421c-182">Requirement</span></span> | <span data-ttu-id="2421c-183">Wert</span><span class="sxs-lookup"><span data-stu-id="2421c-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2421c-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2421c-184">Minimum supported client</span></span><br/> | <span data-ttu-id="2421c-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2421c-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2421c-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2421c-186">Minimum supported server</span></span><br/> | <span data-ttu-id="2421c-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2421c-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2421c-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="2421c-188">Namespace</span></span><br/>                | <span data-ttu-id="2421c-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2421c-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="2421c-190">MOF</span><span class="sxs-lookup"><span data-stu-id="2421c-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2421c-191"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2421c-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2421c-192">DLL</span><span class="sxs-lookup"><span data-stu-id="2421c-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2421c-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2421c-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2421c-194">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2421c-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="2421c-195">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2421c-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2421c-196">**\_Win32-Dienst**</span><span class="sxs-lookup"><span data-stu-id="2421c-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="2421c-197">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="2421c-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="2421c-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="2421c-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

