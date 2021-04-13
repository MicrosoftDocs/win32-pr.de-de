---
title: Delete-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Der Löschvorgang \ 8194; WMI-Klassenmethode löscht einen vorhandenen Dienst.
ms.assetid: 0F012D6B-BD29-4AC3-AC7E-78EC02C1FF43
ms.tgt_platform: multiple
keywords:
- Delete-Methode Remotedesktopdienste
- Delete-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, DELETE-Methode
topic_type:
- apiref
api_name:
- Win32_Service.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89e2c30ef39d7b36baf62a486477fcf4a7fa2842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518923"
---
# <a name="delete-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="014ef-106">Delete-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="014ef-106">Delete method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="014ef-107">Mit der **Delete** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode wird ein vorhandener Dienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="014ef-107">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="014ef-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="014ef-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="014ef-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="014ef-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="014ef-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="014ef-110">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="014ef-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="014ef-111">Parameters</span></span>

<span data-ttu-id="014ef-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="014ef-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="014ef-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="014ef-113">Return value</span></span>

<span data-ttu-id="014ef-114">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="014ef-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="014ef-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="014ef-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="014ef-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="014ef-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="014ef-117">**0**</span><span class="sxs-lookup"><span data-stu-id="014ef-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-118">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="014ef-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-119">**1**</span><span class="sxs-lookup"><span data-stu-id="014ef-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-120">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="014ef-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-121">**2**</span><span class="sxs-lookup"><span data-stu-id="014ef-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-122">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="014ef-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-123">**3**</span><span class="sxs-lookup"><span data-stu-id="014ef-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-124">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="014ef-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-125">**4**</span><span class="sxs-lookup"><span data-stu-id="014ef-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="014ef-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-127">**5**</span><span class="sxs-lookup"><span data-stu-id="014ef-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-128">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="014ef-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-129">**6**</span><span class="sxs-lookup"><span data-stu-id="014ef-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-130">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="014ef-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-131">**7**</span><span class="sxs-lookup"><span data-stu-id="014ef-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-132">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="014ef-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-133">**8**</span><span class="sxs-lookup"><span data-stu-id="014ef-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-134">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="014ef-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-135">**9**</span><span class="sxs-lookup"><span data-stu-id="014ef-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-136">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="014ef-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-137">**10**</span><span class="sxs-lookup"><span data-stu-id="014ef-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-138">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="014ef-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-139">**11**</span><span class="sxs-lookup"><span data-stu-id="014ef-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-140">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="014ef-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-141">**12**</span><span class="sxs-lookup"><span data-stu-id="014ef-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-142">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="014ef-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-143">**13**</span><span class="sxs-lookup"><span data-stu-id="014ef-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-144">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="014ef-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-145">**14**</span><span class="sxs-lookup"><span data-stu-id="014ef-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-146">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="014ef-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-147">**15**</span><span class="sxs-lookup"><span data-stu-id="014ef-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-148">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="014ef-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-149">**16**</span><span class="sxs-lookup"><span data-stu-id="014ef-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-150">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="014ef-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-151">**17**</span><span class="sxs-lookup"><span data-stu-id="014ef-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-152">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="014ef-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-153">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="014ef-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-154">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="014ef-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-155">**19**</span><span class="sxs-lookup"><span data-stu-id="014ef-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-156">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="014ef-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-157">**20**</span><span class="sxs-lookup"><span data-stu-id="014ef-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-158">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="014ef-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-159">**21**</span><span class="sxs-lookup"><span data-stu-id="014ef-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-160">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="014ef-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-161">**22**</span><span class="sxs-lookup"><span data-stu-id="014ef-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-162">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="014ef-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-163">**23**</span><span class="sxs-lookup"><span data-stu-id="014ef-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-164">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="014ef-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-165">**24**</span><span class="sxs-lookup"><span data-stu-id="014ef-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="014ef-166">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="014ef-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="014ef-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="014ef-167">Remarks</span></span>

<span data-ttu-id="014ef-168">Wenn sich Ihre Organisation ändert, können Sie bestimmte Dienste von bestimmten Computern entfernen.</span><span class="sxs-lookup"><span data-stu-id="014ef-168">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="014ef-169">Interne Dienste und Dienste von Drittanbietern können mithilfe von WMI entfernt werden, während die Betriebssystem Dienste mithilfe von Sysocmgr.exe entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="014ef-169">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="014ef-170">Beachten Sie beim Vorbereiten des Entfernens der Dienste die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="014ef-170">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="014ef-171">Dienste müssen beendet werden, bevor Sie Sie entfernen.</span><span class="sxs-lookup"><span data-stu-id="014ef-171">Services must be stopped before you remove them.</span></span> <span data-ttu-id="014ef-172">Wenn der Dienst ausgeführt wird, während Sie den DELETE-Befehl ausgeben, wird der Dienst zum Löschen markiert, er wird jedoch weiterhin ausgeführt, bis er beendet wird und alle geöffneten Handles geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="014ef-172">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="014ef-173">Wenn der Dienst nie beendet wird, wird der Dienst nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="014ef-173">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="014ef-174">Wenn Sie einen Dienst entfernen, wird die ausführbare Datei des dienstanders nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="014ef-174">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="014ef-175">Wenn Sie einen Dienst mithilfe von WMI entfernen, werden die zugehörigen Registrierungseinträge unter HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services gelöscht.</span><span class="sxs-lookup"><span data-stu-id="014ef-175">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="014ef-176">Daher wird der Dienst nicht mehr installiert und ist nicht über das Dienste-Snap-in verfügbar.</span><span class="sxs-lookup"><span data-stu-id="014ef-176">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="014ef-177">Die ausführbare Datei wird von WMI jedoch nicht gelöscht, was bedeutet, dass Sie den Dienst problemlos neu installieren können.</span><span class="sxs-lookup"><span data-stu-id="014ef-177">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="014ef-178">Zum Löschen der ausführbaren Datei müssen Sie den Pfadnamen abrufen und die Datei dann löschen.</span><span class="sxs-lookup"><span data-stu-id="014ef-178">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="014ef-179">Wenn Sie einen Windows 2000-Basis Dienst (z. b. DHCP) mithilfe von WMI entfernen, werden die Registrierungseinträge für diesen Dienst gelöscht. die Verknüpfung wird jedoch nicht aus dem Menü "Verwaltung" entfernt, oder der Dienst wird aus dem Assistenten für Windows-Komponenten entfernt.</span><span class="sxs-lookup"><span data-stu-id="014ef-179">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="014ef-180">Dies kann alle Benutzer verwirren, die versuchen, die Konfiguration des Computers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="014ef-180">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="014ef-181">Wenn Sie den DHCP-Dienst beispielsweise mithilfe eines WMI-Skripts entfernen, wird der DHCP-Dienst nicht mehr im Dienste-Snap-in aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="014ef-181">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="014ef-182">Eine nicht funktionsfähige Verknüpfung mit der DHCP-Konsole verbleibt jedoch im Menü "Verwaltung", und wenn Sie den Assistenten für Windows-Komponenten starten, bedeutet dies, dass der DHCP-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="014ef-182">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="014ef-183">Aus diesem Grund sollten Sie immer Sysocmgr.exe verwenden, um Windows 2000-Dienste Programm gesteuert zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="014ef-183">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="014ef-184">Beispiele</span><span class="sxs-lookup"><span data-stu-id="014ef-184">Examples</span></span>

<span data-ttu-id="014ef-185">Im folgenden VBScript-Codebeispiel wird beschrieben, wie ein Dienst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="014ef-185">The following VBScript code sample describes how to delete a service.</span></span>


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



<span data-ttu-id="014ef-186">Im folgenden perl-Codebeispiel wird beschrieben, wie ein Dienst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="014ef-186">The following Perl code sample describes how to delete a service.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="014ef-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="014ef-187">Requirements</span></span>



| <span data-ttu-id="014ef-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="014ef-188">Requirement</span></span> | <span data-ttu-id="014ef-189">Wert</span><span class="sxs-lookup"><span data-stu-id="014ef-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="014ef-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="014ef-190">Minimum supported client</span></span><br/> | <span data-ttu-id="014ef-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="014ef-191">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="014ef-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="014ef-192">Minimum supported server</span></span><br/> | <span data-ttu-id="014ef-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="014ef-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="014ef-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="014ef-194">Namespace</span></span><br/>                | <span data-ttu-id="014ef-195">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="014ef-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="014ef-196">MOF</span><span class="sxs-lookup"><span data-stu-id="014ef-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="014ef-197"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="014ef-197"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="014ef-198">DLL</span><span class="sxs-lookup"><span data-stu-id="014ef-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="014ef-199"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="014ef-199"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014ef-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="014ef-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014ef-201">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="014ef-201">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="014ef-202">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="014ef-202">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="014ef-203">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="014ef-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="014ef-204">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="014ef-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

