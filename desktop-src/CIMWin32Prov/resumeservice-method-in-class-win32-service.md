---
description: Versucht, den Dienst, auf den verwiesen wird, im Zustand "fortgesetzt"
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: ResumeService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861671"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="20d66-103">ResumeService-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="20d66-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="20d66-104">Die **ResumeService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, den Dienst, auf den verwiesen wird, in den Status "fortgesetzt"</span><span class="sxs-lookup"><span data-stu-id="20d66-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="20d66-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="20d66-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="20d66-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="20d66-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="20d66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="20d66-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="20d66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20d66-108">Parameters</span></span>

<span data-ttu-id="20d66-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="20d66-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20d66-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20d66-110">Return value</span></span>

<span data-ttu-id="20d66-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="20d66-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="20d66-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="20d66-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="20d66-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="20d66-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="20d66-114">**0**</span><span class="sxs-lookup"><span data-stu-id="20d66-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="20d66-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-116">**1**</span><span class="sxs-lookup"><span data-stu-id="20d66-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20d66-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-118">**2**</span><span class="sxs-lookup"><span data-stu-id="20d66-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-119">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="20d66-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-120">**3**</span><span class="sxs-lookup"><span data-stu-id="20d66-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="20d66-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-122">**4**</span><span class="sxs-lookup"><span data-stu-id="20d66-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="20d66-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-124">**5**</span><span class="sxs-lookup"><span data-stu-id="20d66-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-125">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="20d66-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-126">**6**</span><span class="sxs-lookup"><span data-stu-id="20d66-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="20d66-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-128">**7**</span><span class="sxs-lookup"><span data-stu-id="20d66-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="20d66-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-130">**8**</span><span class="sxs-lookup"><span data-stu-id="20d66-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-131">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="20d66-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-132">**9**</span><span class="sxs-lookup"><span data-stu-id="20d66-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-133">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="20d66-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-134">**10**</span><span class="sxs-lookup"><span data-stu-id="20d66-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20d66-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-136">**11**</span><span class="sxs-lookup"><span data-stu-id="20d66-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="20d66-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-138">**12**</span><span class="sxs-lookup"><span data-stu-id="20d66-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-139">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="20d66-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-140">**13**</span><span class="sxs-lookup"><span data-stu-id="20d66-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="20d66-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-142">**14**</span><span class="sxs-lookup"><span data-stu-id="20d66-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="20d66-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-144">**15**</span><span class="sxs-lookup"><span data-stu-id="20d66-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="20d66-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-146">**16**</span><span class="sxs-lookup"><span data-stu-id="20d66-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="20d66-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-148">**17**</span><span class="sxs-lookup"><span data-stu-id="20d66-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-149">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="20d66-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-150">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="20d66-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-151">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="20d66-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-152">**19**</span><span class="sxs-lookup"><span data-stu-id="20d66-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-153">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20d66-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-154">**20**</span><span class="sxs-lookup"><span data-stu-id="20d66-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-155">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="20d66-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-156">**21**</span><span class="sxs-lookup"><span data-stu-id="20d66-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-157">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="20d66-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-158">**22**</span><span class="sxs-lookup"><span data-stu-id="20d66-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="20d66-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-160">**23**</span><span class="sxs-lookup"><span data-stu-id="20d66-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20d66-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="20d66-162">**24**</span><span class="sxs-lookup"><span data-stu-id="20d66-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="20d66-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="20d66-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20d66-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20d66-164">Remarks</span></span>

<span data-ttu-id="20d66-165">Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst gibt, werden die beiden Zustände anders als der SCM angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20d66-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="20d66-166">Ein angehaltener Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienst Start Prozedur durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="20d66-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="20d66-167">Ein angehaltene Dienst wird jedoch weiterhin ausgeführt, aber seine funktionstüchtig ist angehalten.</span><span class="sxs-lookup"><span data-stu-id="20d66-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="20d66-168">Aus diesem Grund muss ein angehaltene Dienst nicht die gesamte Dienst Start Prozedur durchlaufen, sondern erfordert ein anderes Verfahren, um die Funktionsweise fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="20d66-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="20d66-169">Sie müssen die richtige-Methode verwenden, um einen Dienst zu starten, der angehalten wurde, oder um einen Dienst fortzusetzen, der angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="20d66-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="20d66-170">Die [**Win32- \_ Dienst**](win32-service.md) Methoden " [**StartService**](startservice-method-in-class-win32-service.md) " und " **ResumeService** " sollten in den folgenden Situationen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="20d66-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="20d66-171">Wenn ein Dienst aktuell beendet ist, müssen Sie ihn mit der [**Start Service**](startservice-method-in-class-win32-service.md) -Methode neu starten. **ResumeService** kann einen Dienst nicht starten, der zurzeit beendet ist.</span><span class="sxs-lookup"><span data-stu-id="20d66-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="20d66-172">Wenn ein Dienst angehalten wird, müssen Sie **ResumeService** verwenden.</span><span class="sxs-lookup"><span data-stu-id="20d66-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="20d66-173">Wenn Sie die [**Start Service**](startservice-method-in-class-win32-service.md) -Methode für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "der Dienst wird bereits ausgeführt."</span><span class="sxs-lookup"><span data-stu-id="20d66-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="20d66-174">Der Dienst bleibt jedoch angehalten, bis der Steuerungs Code zum Fortsetzen des dienstandens an ihn gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="20d66-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="20d66-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20d66-175">Examples</span></span>

<span data-ttu-id="20d66-176">Das Beispiel zum fort [setzen von Autostart-Diensten mit angehaltenen](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript startet alle automatischen Start Dienste neu, die angehalten wurden.</span><span class="sxs-lookup"><span data-stu-id="20d66-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="20d66-177">Im folgenden VBScript-Codebeispiel wird beschrieben, wie Sie einen angehaltenen Dienst aus Instanzen des [**Win32- \_ Dienstanbieter**](win32-service.md)fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="20d66-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="20d66-178">Der Dienst muss angehalten und bereits ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="20d66-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



<span data-ttu-id="20d66-179">Im folgenden perl-Codebeispiel wird beschrieben, wie ein angehaltene Dienst von Instanzen des [**Win32- \_ Dienstanbieter**](win32-service.md)fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="20d66-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="20d66-180">Der Dienst muss angehalten und bereits ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="20d66-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="20d66-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20d66-181">Requirements</span></span>



| <span data-ttu-id="20d66-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20d66-182">Requirement</span></span> | <span data-ttu-id="20d66-183">Wert</span><span class="sxs-lookup"><span data-stu-id="20d66-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20d66-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20d66-184">Minimum supported client</span></span><br/> | <span data-ttu-id="20d66-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20d66-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20d66-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20d66-186">Minimum supported server</span></span><br/> | <span data-ttu-id="20d66-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20d66-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20d66-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="20d66-188">Namespace</span></span><br/>                | <span data-ttu-id="20d66-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="20d66-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="20d66-190">MOF</span><span class="sxs-lookup"><span data-stu-id="20d66-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20d66-191"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="20d66-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20d66-192">DLL</span><span class="sxs-lookup"><span data-stu-id="20d66-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20d66-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20d66-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20d66-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20d66-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="20d66-195">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20d66-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="20d66-196">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="20d66-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="20d66-197">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="20d66-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

