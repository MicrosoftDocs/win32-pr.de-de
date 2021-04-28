---
description: Delete-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter) – Der Delete&\# 8194; Die WMI-Klassenmethode löscht einen vorhandenen Dienst.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4031184e23e99fc54237ed0b0b4196fe6c075c5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089578"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ed215-103">Delete-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="ed215-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ed215-104">Die **Delete** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht einen vorhandenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="ed215-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="ed215-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed215-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ed215-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="ed215-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed215-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed215-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="ed215-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed215-108">Parameters</span></span>

<span data-ttu-id="ed215-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed215-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed215-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed215-110">Return value</span></span>

<span data-ttu-id="ed215-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um auf einen Fehler hindeuten zu können.</span><span class="sxs-lookup"><span data-stu-id="ed215-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="ed215-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ed215-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ed215-113">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ed215-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ed215-114">**0**</span><span class="sxs-lookup"><span data-stu-id="ed215-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="ed215-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-116">**1**</span><span class="sxs-lookup"><span data-stu-id="ed215-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed215-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-118">**2**</span><span class="sxs-lookup"><span data-stu-id="ed215-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-119">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ed215-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-120">**3**</span><span class="sxs-lookup"><span data-stu-id="ed215-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ed215-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-122">**4**</span><span class="sxs-lookup"><span data-stu-id="ed215-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="ed215-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-124">**5**</span><span class="sxs-lookup"><span data-stu-id="ed215-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-125">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="ed215-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-126">**6**</span><span class="sxs-lookup"><span data-stu-id="ed215-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="ed215-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-128">**7**</span><span class="sxs-lookup"><span data-stu-id="ed215-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="ed215-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-130">**8**</span><span class="sxs-lookup"><span data-stu-id="ed215-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-131">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="ed215-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-132">**9**</span><span class="sxs-lookup"><span data-stu-id="ed215-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-133">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ed215-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-134">**10**</span><span class="sxs-lookup"><span data-stu-id="ed215-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed215-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-136">**11**</span><span class="sxs-lookup"><span data-stu-id="ed215-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="ed215-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-138">**12**</span><span class="sxs-lookup"><span data-stu-id="ed215-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-139">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ed215-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-140">**13**</span><span class="sxs-lookup"><span data-stu-id="ed215-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ed215-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-142">**14**</span><span class="sxs-lookup"><span data-stu-id="ed215-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ed215-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-144">**15**</span><span class="sxs-lookup"><span data-stu-id="ed215-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ed215-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-146">**16**</span><span class="sxs-lookup"><span data-stu-id="ed215-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ed215-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-148">**17**</span><span class="sxs-lookup"><span data-stu-id="ed215-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-149">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="ed215-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-150">**18**</span><span class="sxs-lookup"><span data-stu-id="ed215-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-151">Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="ed215-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-152">**19**</span><span class="sxs-lookup"><span data-stu-id="ed215-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-153">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed215-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-154">**20**</span><span class="sxs-lookup"><span data-stu-id="ed215-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-155">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ed215-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-156">**21**</span><span class="sxs-lookup"><span data-stu-id="ed215-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-157">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="ed215-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-158">**22**</span><span class="sxs-lookup"><span data-stu-id="ed215-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="ed215-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-160">**23**</span><span class="sxs-lookup"><span data-stu-id="ed215-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ed215-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ed215-162">**24**</span><span class="sxs-lookup"><span data-stu-id="ed215-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ed215-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="ed215-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed215-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed215-164">Remarks</span></span>

<span data-ttu-id="ed215-165">Wenn sich Ihre Organisation ändert, können Sie bestimmte Dienste von bestimmten Computern entfernen.</span><span class="sxs-lookup"><span data-stu-id="ed215-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="ed215-166">In- und Drittanbieterdienste können mithilfe von WMI entfernt werden, während Betriebssystemdienste mithilfe von Sysocmgr.exe entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="ed215-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="ed215-167">Beachten Sie beim Vorbereiten des Entfernens von Diensten die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="ed215-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="ed215-168">Dienste müssen beendet werden, bevor Sie sie entfernen.</span><span class="sxs-lookup"><span data-stu-id="ed215-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="ed215-169">Wenn der Dienst ausgeführt wird, wenn Sie den Löschbefehl ausstellen, wird der Dienst zum Löschen markiert, aber er wird weiterhin ausgeführt, bis er beendet wird und alle geöffneten Handles geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ed215-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="ed215-170">Wenn der Dienst nie beendet wird, wird dieser Dienst nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ed215-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="ed215-171">Durch das Entfernen eines Diensts wird die ausführbare Datei des Diensts nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="ed215-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="ed215-172">Wenn Sie einen Dienst mithilfe von WMI entfernen, werden die zugehörigen Registrierungseinträge unter HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ Services gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ed215-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="ed215-173">Daher ist der Dienst nicht mehr installiert und über das Dienst-Snap-In nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed215-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="ed215-174">WMI löscht die ausführbare Datei jedoch nicht, was bedeutet, dass Sie den Dienst problemlos neu installieren können.</span><span class="sxs-lookup"><span data-stu-id="ed215-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="ed215-175">Um die ausführbare Datei zu löschen, müssen Sie den Pfadnamen abrufen und dann die Datei löschen.</span><span class="sxs-lookup"><span data-stu-id="ed215-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="ed215-176">Wenn Sie einen Windows 2000-Basisdienst (z. B. DHCP) mithilfe von WMI entfernen, werden die Registrierungseinträge für diesen Dienst gelöscht, aber die Verknüpfung wird nicht aus dem Menü Verwaltung entfernt, und der Dienst wird nicht aus dem Windows-Komponenten-Assistenten entfernt.</span><span class="sxs-lookup"><span data-stu-id="ed215-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="ed215-177">Dies kann jeden verwirren, der versucht, zu bestimmen, wie der Computer konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ed215-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="ed215-178">Wenn Sie beispielsweise den DHCP-Dienst mithilfe eines WMI-Skripts entfernen, wird der DHCP-Dienst nicht mehr im Dienst-Snap-In aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed215-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="ed215-179">Eine nicht funktionierende Verknüpfung mit der DHCP-Konsole verbleibt jedoch im Menü Verwaltung. Wenn Sie den Windows-Komponenten-Assistenten starten, wird angezeigt, dass der DHCP-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed215-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="ed215-180">Aus diesem Grund sollten Sie immer Sysocmgr.exe verwenden, um Windows 2000-Dienste programmgesteuert zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ed215-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="ed215-181">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed215-181">Examples</span></span>

<span data-ttu-id="ed215-182">Im folgenden VBScript-Codebeispiel wird das Löschen eines Diensts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed215-182">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="ed215-183">Im folgenden Perl-Codebeispiel wird das Löschen eines Diensts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed215-183">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="ed215-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed215-184">Requirements</span></span>



| <span data-ttu-id="ed215-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed215-185">Requirement</span></span> | <span data-ttu-id="ed215-186">Wert</span><span class="sxs-lookup"><span data-stu-id="ed215-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed215-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed215-187">Minimum supported client</span></span><br/> | <span data-ttu-id="ed215-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed215-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed215-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed215-189">Minimum supported server</span></span><br/> | <span data-ttu-id="ed215-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed215-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed215-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed215-191">Namespace</span></span><br/>                | <span data-ttu-id="ed215-192">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="ed215-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed215-193">MOF</span><span class="sxs-lookup"><span data-stu-id="ed215-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed215-194"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed215-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed215-195">DLL</span><span class="sxs-lookup"><span data-stu-id="ed215-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed215-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed215-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed215-197">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed215-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed215-198">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed215-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ed215-199">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="ed215-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="ed215-200">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="ed215-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

