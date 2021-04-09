---
description: Versucht, den referenzierten Dienst in seinen Startzustand zu versetzen.
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Start Service-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb530766781de4e23cc86778c1597a5c5c2a1014
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958382"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="b667f-103">Start Service-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="b667f-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b667f-104">Die **Start Service** -Methode versucht, den Dienst, auf den verwiesen wird, in den Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="b667f-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="b667f-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b667f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b667f-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b667f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b667f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b667f-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="b667f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b667f-108">Parameters</span></span>

<span data-ttu-id="b667f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b667f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b667f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b667f-110">Return value</span></span>

<span data-ttu-id="b667f-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b667f-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="b667f-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b667f-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b667f-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b667f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b667f-114">**0**</span><span class="sxs-lookup"><span data-stu-id="b667f-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b667f-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-116">**1**</span><span class="sxs-lookup"><span data-stu-id="b667f-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b667f-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-118">**2**</span><span class="sxs-lookup"><span data-stu-id="b667f-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-119">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="b667f-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-120">**3**</span><span class="sxs-lookup"><span data-stu-id="b667f-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="b667f-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-122">**4**</span><span class="sxs-lookup"><span data-stu-id="b667f-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="b667f-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-124">**5**</span><span class="sxs-lookup"><span data-stu-id="b667f-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-125">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="b667f-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-126">**6**</span><span class="sxs-lookup"><span data-stu-id="b667f-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="b667f-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-128">**7**</span><span class="sxs-lookup"><span data-stu-id="b667f-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="b667f-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-130">**8**</span><span class="sxs-lookup"><span data-stu-id="b667f-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-131">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b667f-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-132">**9**</span><span class="sxs-lookup"><span data-stu-id="b667f-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-133">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b667f-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-134">**10**</span><span class="sxs-lookup"><span data-stu-id="b667f-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b667f-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-136">**11**</span><span class="sxs-lookup"><span data-stu-id="b667f-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b667f-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-138">**12**</span><span class="sxs-lookup"><span data-stu-id="b667f-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-139">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="b667f-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-140">**13**</span><span class="sxs-lookup"><span data-stu-id="b667f-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b667f-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-142">**14**</span><span class="sxs-lookup"><span data-stu-id="b667f-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b667f-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-144">**15**</span><span class="sxs-lookup"><span data-stu-id="b667f-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="b667f-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-146">**16**</span><span class="sxs-lookup"><span data-stu-id="b667f-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="b667f-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-148">**17**</span><span class="sxs-lookup"><span data-stu-id="b667f-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-149">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="b667f-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-150">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="b667f-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-151">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b667f-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-152">**19**</span><span class="sxs-lookup"><span data-stu-id="b667f-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-153">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b667f-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-154">**20**</span><span class="sxs-lookup"><span data-stu-id="b667f-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-155">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b667f-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-156">**21**</span><span class="sxs-lookup"><span data-stu-id="b667f-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-157">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b667f-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-158">**22**</span><span class="sxs-lookup"><span data-stu-id="b667f-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b667f-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-160">**23**</span><span class="sxs-lookup"><span data-stu-id="b667f-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b667f-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b667f-162">**24**</span><span class="sxs-lookup"><span data-stu-id="b667f-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b667f-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="b667f-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b667f-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b667f-164">Remarks</span></span>

<span data-ttu-id="b667f-165">Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst gibt, werden die beiden Zustände anders als der SCM angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b667f-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="b667f-166">Ein angehaltener Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienst Start Prozedur durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="b667f-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="b667f-167">Ein angehaltene Dienst wird jedoch weiterhin ausgeführt, aber seine funktionstüchtig ist angehalten.</span><span class="sxs-lookup"><span data-stu-id="b667f-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="b667f-168">Aus diesem Grund muss ein angehaltene Dienst nicht die gesamte Dienst Start Prozedur durchlaufen, sondern erfordert ein anderes Verfahren, um die Funktionsweise fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b667f-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="b667f-169">Sie müssen die richtige-Methode verwenden, um einen Dienst zu starten, der angehalten wurde, oder um einen Dienst fortzusetzen, der angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="b667f-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="b667f-170">Die [**Win32- \_ Dienst**](win32-service.md) Methoden " **StartService** " und " [**ResumeService**](resumeservice-method-in-class-win32-service.md) " sollten in den folgenden Situationen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="b667f-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="b667f-171">Wenn ein Dienst aktuell beendet ist, müssen Sie ihn mit der **Start Service** -Methode neu starten. [**ResumeService**](resumeservice-method-in-class-win32-service.md) kann einen Dienst nicht starten, der zurzeit beendet ist.</span><span class="sxs-lookup"><span data-stu-id="b667f-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="b667f-172">Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](resumeservice-method-in-class-win32-service.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="b667f-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="b667f-173">Wenn Sie die **Start Service** -Methode für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "der Dienst wird bereits ausgeführt."</span><span class="sxs-lookup"><span data-stu-id="b667f-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="b667f-174">Der Dienst bleibt jedoch angehalten, bis der Steuerungs Code zum Fortsetzen des dienstandens an ihn gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b667f-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="b667f-175">Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängt, werden beide Dienste gestartet.</span><span class="sxs-lookup"><span data-stu-id="b667f-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="b667f-176">Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="b667f-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="b667f-177">Sie müssen die Association-Klasse [**Win32 \_ dependentservice**](win32-dependentservice.md) und die [assoziatoren von](/windows/desktop/WmiSdk/associators-of-statement) Query verwenden, um die abhängigen Elemente zu suchen und Sie separat zu starten.</span><span class="sxs-lookup"><span data-stu-id="b667f-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="b667f-178">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b667f-178">Examples</span></span>

<span data-ttu-id="b667f-179">Das [Remote enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell-Beispiel aktiviert Remote den Remotedesktop-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b667f-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="b667f-180">Das PowerShell-Beispiel zum [beenden, starten, aktivieren oder Deaktivieren des Dienstanbieter](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) startet, beendet, aktiviert oder deaktiviert einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="b667f-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="b667f-181">Im folgenden vbsscript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32- \_ diensdienstanbieter**](win32-service.md)gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b667f-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="b667f-182">Im folgenden perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32- \_ Dienstanbieter**](win32-service.md)gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b667f-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="b667f-183">Das folgende VBScript-Codebeispiel (NetDDE) ist vom NetDDEDSDM-Dienst abhängig.</span><span class="sxs-lookup"><span data-stu-id="b667f-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="b667f-184">Das Skript findet die Klasse, von der NetDDE abhängt, und startet Sie, wodurch NetDDE nicht automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b667f-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="b667f-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b667f-185">Requirements</span></span>



| <span data-ttu-id="b667f-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b667f-186">Requirement</span></span> | <span data-ttu-id="b667f-187">Wert</span><span class="sxs-lookup"><span data-stu-id="b667f-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b667f-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b667f-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b667f-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b667f-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b667f-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b667f-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b667f-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b667f-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b667f-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="b667f-192">Namespace</span></span><br/>                | <span data-ttu-id="b667f-193">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b667f-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b667f-194">MOF</span><span class="sxs-lookup"><span data-stu-id="b667f-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b667f-195"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b667f-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b667f-196">DLL</span><span class="sxs-lookup"><span data-stu-id="b667f-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b667f-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b667f-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b667f-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b667f-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="b667f-199">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b667f-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b667f-200">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="b667f-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="b667f-201">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="b667f-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

