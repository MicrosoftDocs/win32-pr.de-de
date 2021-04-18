---
description: Versetzt den Dienst, der durch das Win32- \_ Dienst Objekt dargestellt wird, in den Zustand "beendet".
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Stop Service-Methode der Win32_Service-Klasse (sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344960"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="c57fc-103">Stop Service-Methode der Win32_Service-Klasse (sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="c57fc-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="c57fc-104">Die **StopService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versetzt den Dienst, der durch das Win32- [**\_ Dienst**](win32-service.md) Objekt dargestellt wird, in den Zustand "beendet".</span><span class="sxs-lookup"><span data-stu-id="c57fc-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="c57fc-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c57fc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c57fc-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c57fc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c57fc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c57fc-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="c57fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c57fc-108">Parameters</span></span>

<span data-ttu-id="c57fc-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c57fc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c57fc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c57fc-110">Return value</span></span>

<span data-ttu-id="c57fc-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c57fc-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c57fc-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c57fc-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c57fc-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c57fc-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c57fc-114">**0**</span><span class="sxs-lookup"><span data-stu-id="c57fc-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c57fc-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-116">**1**</span><span class="sxs-lookup"><span data-stu-id="c57fc-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-118">**2**</span><span class="sxs-lookup"><span data-stu-id="c57fc-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-119">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c57fc-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-120">**3**</span><span class="sxs-lookup"><span data-stu-id="c57fc-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c57fc-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-122">**4**</span><span class="sxs-lookup"><span data-stu-id="c57fc-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="c57fc-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-124">**5**</span><span class="sxs-lookup"><span data-stu-id="c57fc-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-125">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="c57fc-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-126">**6**</span><span class="sxs-lookup"><span data-stu-id="c57fc-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c57fc-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-128">**7**</span><span class="sxs-lookup"><span data-stu-id="c57fc-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="c57fc-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-130">**8**</span><span class="sxs-lookup"><span data-stu-id="c57fc-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-131">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c57fc-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-132">**9**</span><span class="sxs-lookup"><span data-stu-id="c57fc-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-133">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c57fc-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-134">**10**</span><span class="sxs-lookup"><span data-stu-id="c57fc-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-136">**11**</span><span class="sxs-lookup"><span data-stu-id="c57fc-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-138">**12**</span><span class="sxs-lookup"><span data-stu-id="c57fc-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-139">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-140">**13**</span><span class="sxs-lookup"><span data-stu-id="c57fc-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c57fc-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-142">**14**</span><span class="sxs-lookup"><span data-stu-id="c57fc-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c57fc-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-144">**15**</span><span class="sxs-lookup"><span data-stu-id="c57fc-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c57fc-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-146">**16**</span><span class="sxs-lookup"><span data-stu-id="c57fc-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-148">**17**</span><span class="sxs-lookup"><span data-stu-id="c57fc-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-149">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="c57fc-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-150">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="c57fc-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-151">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c57fc-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-152">**19**</span><span class="sxs-lookup"><span data-stu-id="c57fc-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-153">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-154">**20**</span><span class="sxs-lookup"><span data-stu-id="c57fc-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-155">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c57fc-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-156">**21**</span><span class="sxs-lookup"><span data-stu-id="c57fc-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-157">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-158">**22**</span><span class="sxs-lookup"><span data-stu-id="c57fc-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c57fc-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-160">**23**</span><span class="sxs-lookup"><span data-stu-id="c57fc-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c57fc-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c57fc-162">**24**</span><span class="sxs-lookup"><span data-stu-id="c57fc-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c57fc-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="c57fc-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c57fc-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c57fc-164">Remarks</span></span>

<span data-ttu-id="c57fc-165">Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die-Methode **StopService** und die [**anhaleservice**](pauseservice-method-in-class-win32-systemdriver.md) -Methode verwenden, um-Dienste anzuhalten und anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="c57fc-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="c57fc-166">Die Entscheidung, einen Dienst zu stoppen, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="c57fc-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="c57fc-167">Ist der Dienst in der Lage, angehalten zu werden?</span><span class="sxs-lookup"><span data-stu-id="c57fc-167">Is the service capable of being paused?</span></span> <span data-ttu-id="c57fc-168">Wenn dies nicht der Wert ist, ist die einzige Option der Dienst wird beendet.</span><span class="sxs-lookup"><span data-stu-id="c57fc-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="c57fc-169">Müssen Sie die Verarbeitung von Client Anforderungen für alle Benutzer fortsetzen, die bereits mit dem Dienst verbunden sind?</span><span class="sxs-lookup"><span data-stu-id="c57fc-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="c57fc-170">Wenn dies der Fall ist, ermöglicht das Anhalten eines Dienstanbieter in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert</span><span class="sxs-lookup"><span data-stu-id="c57fc-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="c57fc-171">Wenn Sie einen Dienst beenden, werden dagegen alle Clients sofort getrennt.</span><span class="sxs-lookup"><span data-stu-id="c57fc-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="c57fc-172">Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden?</span><span class="sxs-lookup"><span data-stu-id="c57fc-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="c57fc-173">Obwohl Dienst Eigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten nicht wirksam, bis der Dienst tatsächlich beendet und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c57fc-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="c57fc-174">Der zum Anhalten eines Dienstanbieter erforderliche Skriptcode ist nahezu identisch mit dem Code, der zum Anhalten des Dienstanbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c57fc-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="c57fc-175">Wenn Sie versuchen, einen Dienst zu beenden, für den abhängige Dienste ausgeführt werden, schlägt die **Stop Service** -Methode mit einem Rückgabewert von 3 fehl.</span><span class="sxs-lookup"><span data-stu-id="c57fc-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="c57fc-176">Die abhängigen Dienste müssen zuerst beendet werden.</span><span class="sxs-lookup"><span data-stu-id="c57fc-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="c57fc-177">Wenn Sie einen Dienst abbrechen, überprüfen Sie den [**Win32- \_ Dienst**](win32-service.md)sofort.**State** -Eigenschaft, da der Dienst möglicherweise weiterhin als wird ausgeführt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c57fc-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="c57fc-178">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c57fc-178">Examples</span></span>

<span data-ttu-id="c57fc-179">[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell-Beispiel legt den Dienststatus für Remote Computer fest.</span><span class="sxs-lookup"><span data-stu-id="c57fc-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="c57fc-180">Das Beispiel zum [Beenden eines Diensts und seiner abhängigen](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript beendet einen Dienst und alle abhängigen Dienste.</span><span class="sxs-lookup"><span data-stu-id="c57fc-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="c57fc-181">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein Dienst heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c57fc-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="c57fc-182">Im folgenden perl-Codebeispiel wird veranschaulicht, wie ein Dienst heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c57fc-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="c57fc-183">Das folgende VBScript-Codebeispiel zeigt, dass Sie den NetDDE-Dienst erst beenden können, wenn die abhängigen Dienste beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c57fc-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="c57fc-184">Stellen Sie zum Ausführen des Skripts sicher, dass der NetDDE-Dienst und die zugehörigen abhängigen Dienste über das MMC-Snap-in "Services. msc" oder den Befehl **net Start** ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c57fc-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="c57fc-185">Die [**Win32 \_ dependentservice**](win32-dependentservice.md) -Klasse ermöglicht das Auffinden von Dienst Abhängigkeiten über einen [assoziator von](/windows/desktop/WmiSdk/associators-of-statement) Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c57fc-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="c57fc-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c57fc-186">Requirements</span></span>



| <span data-ttu-id="c57fc-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c57fc-187">Requirement</span></span> | <span data-ttu-id="c57fc-188">Wert</span><span class="sxs-lookup"><span data-stu-id="c57fc-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c57fc-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c57fc-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c57fc-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c57fc-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c57fc-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c57fc-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c57fc-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c57fc-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c57fc-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="c57fc-193">Namespace</span></span><br/>                | <span data-ttu-id="c57fc-194">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c57fc-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c57fc-195">Header</span><span class="sxs-lookup"><span data-stu-id="c57fc-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57fc-196"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57fc-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="c57fc-197">MOF</span><span class="sxs-lookup"><span data-stu-id="c57fc-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c57fc-198"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c57fc-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c57fc-199">DLL</span><span class="sxs-lookup"><span data-stu-id="c57fc-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c57fc-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c57fc-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57fc-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c57fc-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="c57fc-202">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c57fc-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c57fc-203">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c57fc-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c57fc-204">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="c57fc-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="c57fc-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="c57fc-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

