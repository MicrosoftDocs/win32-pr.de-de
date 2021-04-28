---
description: 'StartService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter): Versucht, den Referenzdienst in seinen Startzustand zu stellen.'
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: StartService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)
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
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086158"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="db9c9-103">StartService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="db9c9-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="db9c9-104">Die **StartService-Methode** versucht, den Dienst, auf den verwiesen wird, in seinen Startzustand zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="db9c9-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="db9c9-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="db9c9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db9c9-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="db9c9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db9c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="db9c9-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="db9c9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="db9c9-108">Parameters</span></span>

<span data-ttu-id="db9c9-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="db9c9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db9c9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db9c9-110">Return value</span></span>

<span data-ttu-id="db9c9-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="db9c9-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="db9c9-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="db9c9-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="db9c9-113">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="db9c9-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="db9c9-114">**0**</span><span class="sxs-lookup"><span data-stu-id="db9c9-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="db9c9-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-116">**1**</span><span class="sxs-lookup"><span data-stu-id="db9c9-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db9c9-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-118">**2**</span><span class="sxs-lookup"><span data-stu-id="db9c9-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-119">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="db9c9-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-120">**3**</span><span class="sxs-lookup"><span data-stu-id="db9c9-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="db9c9-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-122">**4**</span><span class="sxs-lookup"><span data-stu-id="db9c9-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="db9c9-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-124">**5**</span><span class="sxs-lookup"><span data-stu-id="db9c9-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-125">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="db9c9-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-126">**6**</span><span class="sxs-lookup"><span data-stu-id="db9c9-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="db9c9-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-128">**7**</span><span class="sxs-lookup"><span data-stu-id="db9c9-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="db9c9-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-130">**8**</span><span class="sxs-lookup"><span data-stu-id="db9c9-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-131">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="db9c9-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-132">**9**</span><span class="sxs-lookup"><span data-stu-id="db9c9-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-133">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="db9c9-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-134">**10**</span><span class="sxs-lookup"><span data-stu-id="db9c9-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db9c9-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-136">**11**</span><span class="sxs-lookup"><span data-stu-id="db9c9-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="db9c9-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-138">**12**</span><span class="sxs-lookup"><span data-stu-id="db9c9-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-139">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="db9c9-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-140">**13**</span><span class="sxs-lookup"><span data-stu-id="db9c9-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="db9c9-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-142">**14**</span><span class="sxs-lookup"><span data-stu-id="db9c9-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="db9c9-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-144">**15**</span><span class="sxs-lookup"><span data-stu-id="db9c9-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="db9c9-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-146">**16**</span><span class="sxs-lookup"><span data-stu-id="db9c9-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="db9c9-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-148">**17**</span><span class="sxs-lookup"><span data-stu-id="db9c9-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-149">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="db9c9-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-150">**18**</span><span class="sxs-lookup"><span data-stu-id="db9c9-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-151">Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="db9c9-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-152">**19**</span><span class="sxs-lookup"><span data-stu-id="db9c9-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-153">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db9c9-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-154">**20**</span><span class="sxs-lookup"><span data-stu-id="db9c9-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-155">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db9c9-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-156">**21**</span><span class="sxs-lookup"><span data-stu-id="db9c9-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-157">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="db9c9-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-158">**22**</span><span class="sxs-lookup"><span data-stu-id="db9c9-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="db9c9-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-160">**23**</span><span class="sxs-lookup"><span data-stu-id="db9c9-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="db9c9-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="db9c9-162">**24**</span><span class="sxs-lookup"><span data-stu-id="db9c9-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="db9c9-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="db9c9-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db9c9-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db9c9-164">Remarks</span></span>

<span data-ttu-id="db9c9-165">Es scheint zwar keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst zu geben, aber die beiden Zustände unterscheiden sich vom SCM.</span><span class="sxs-lookup"><span data-stu-id="db9c9-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="db9c9-166">Ein beendeter Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienststartprozedur durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="db9c9-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="db9c9-167">Ein angehaltener Dienst wird jedoch weiterhin ausgeführt, aber seine Funktion wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="db9c9-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="db9c9-168">Aus diesem Grund muss ein angehaltener Dienst nicht die gesamte Dienststartprozedur durchlaufen, sondern eine andere Prozedur, um die Funktionsweise fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db9c9-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="db9c9-169">Sie müssen die richtige Methode verwenden, um einen angehaltenen Dienst zu starten oder einen angehaltenen Dienst fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db9c9-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="db9c9-170">Die [**Win32-Dienstmethoden \_**](win32-service.md) **StartService** und [**ResumeService**](resumeservice-method-in-class-win32-service.md) sollten in den folgenden Situationen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="db9c9-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="db9c9-171">Wenn ein Dienst derzeit beendet wird, müssen Sie ihn mithilfe der **StartService-Methode** neu starten. [**ResumeService**](resumeservice-method-in-class-win32-service.md) kann einen Dienst, der derzeit beendet ist, nicht starten.</span><span class="sxs-lookup"><span data-stu-id="db9c9-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="db9c9-172">Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](resumeservice-method-in-class-win32-service.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="db9c9-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="db9c9-173">Wenn Sie die **StartService-Methode** für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "Der Dienst wird bereits ausgeführt."</span><span class="sxs-lookup"><span data-stu-id="db9c9-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="db9c9-174">Der Dienst bleibt jedoch angehalten, bis der Dienststeuerungscode zum Fortsetzen an ihn gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="db9c9-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="db9c9-175">Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängig ist, werden beide Dienste gestartet.</span><span class="sxs-lookup"><span data-stu-id="db9c9-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="db9c9-176">Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="db9c9-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="db9c9-177">Sie müssen die Zuordnungsklasse [**Win32 \_ DependentService**](win32-dependentservice.md) und die [Associators Of-Abfrage](/windows/desktop/WmiSdk/associators-of-statement) verwenden, um die Abhängigen zu suchen und separat zu starten.</span><span class="sxs-lookup"><span data-stu-id="db9c9-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="db9c9-178">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db9c9-178">Examples</span></span>

<span data-ttu-id="db9c9-179">Das [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell-Beispiel aktiviert remote den Remotedesktop Dienst.</span><span class="sxs-lookup"><span data-stu-id="db9c9-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="db9c9-180">Das PowerShell-Beispiel ["Dienst beenden", "Starten", "Aktivieren" oder "Deaktivieren"](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) startet, beendet, aktiviert oder deaktiviert einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="db9c9-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="db9c9-181">Im folgenden VBSScript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32-Diensts gestartet \_ wird.**](win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="db9c9-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="db9c9-182">Im folgenden Perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32-Diensts gestartet \_ wird.**](win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="db9c9-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


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



<span data-ttu-id="db9c9-183">Das folgende VBScript-Codebeispiel, NetDDE, ist vom NetDDEDSDM-Dienst abhängig.</span><span class="sxs-lookup"><span data-stu-id="db9c9-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="db9c9-184">Das Skript sucht die Klasse, von der NetDDE abhängt, und startet sie, wodurch NetDDE nicht automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="db9c9-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="db9c9-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db9c9-185">Requirements</span></span>



| <span data-ttu-id="db9c9-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db9c9-186">Requirement</span></span> | <span data-ttu-id="db9c9-187">Wert</span><span class="sxs-lookup"><span data-stu-id="db9c9-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db9c9-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db9c9-188">Minimum supported client</span></span><br/> | <span data-ttu-id="db9c9-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db9c9-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db9c9-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db9c9-190">Minimum supported server</span></span><br/> | <span data-ttu-id="db9c9-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db9c9-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db9c9-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="db9c9-192">Namespace</span></span><br/>                | <span data-ttu-id="db9c9-193">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="db9c9-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db9c9-194">MOF</span><span class="sxs-lookup"><span data-stu-id="db9c9-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db9c9-195"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="db9c9-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db9c9-196">DLL</span><span class="sxs-lookup"><span data-stu-id="db9c9-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9c9-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db9c9-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db9c9-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db9c9-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="db9c9-199">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db9c9-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="db9c9-200">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="db9c9-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="db9c9-201">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="db9c9-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

