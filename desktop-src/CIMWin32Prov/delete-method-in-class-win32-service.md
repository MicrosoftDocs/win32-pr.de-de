---
description: Der Lösch&\# 8194; WMI-Klassenmethode löscht einen vorhandenen Dienst.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
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
ms.openlocfilehash: d06301c3620e144d72c2d4c4f3d8bc90e642374a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214178"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="0c3c4-103">Delete-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="0c3c4-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0c3c4-104">Mit der **Delete** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode wird ein vorhandener Dienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="0c3c4-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0c3c4-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0c3c4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c3c4-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="0c3c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c3c4-108">Parameters</span></span>

<span data-ttu-id="0c3c4-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c3c4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c3c4-110">Return value</span></span>

<span data-ttu-id="0c3c4-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="0c3c4-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0c3c4-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0c3c4-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0c3c4-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0c3c4-114">**0**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-115">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-116">**1**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-118">**2**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-119">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-120">**3**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-121">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-122">**4**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-123">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-124">**5**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-125">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-126">**6**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-127">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-128">**7**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-129">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-130">**8**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-131">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-132">**9**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-133">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-134">**10**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-135">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-136">**11**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-137">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-138">**12**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-139">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-140">**13**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-141">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-142">**14**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-143">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-144">**15**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-145">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-146">**16**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-147">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-148">**17**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-149">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-150">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-151">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-152">**19**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-153">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-154">**20**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-155">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-156">**21**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-157">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-158">**22**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-159">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-160">**23**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-161">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0c3c4-162">**24**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0c3c4-163">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c3c4-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c3c4-164">Remarks</span></span>

<span data-ttu-id="0c3c4-165">Wenn sich Ihre Organisation ändert, können Sie bestimmte Dienste von bestimmten Computern entfernen.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="0c3c4-166">Interne Dienste und Dienste von Drittanbietern können mithilfe von WMI entfernt werden, während die Betriebssystem Dienste mithilfe von Sysocmgr.exe entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="0c3c4-167">Beachten Sie beim Vorbereiten des Entfernens der Dienste die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="0c3c4-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="0c3c4-168">Dienste müssen beendet werden, bevor Sie Sie entfernen.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="0c3c4-169">Wenn der Dienst ausgeführt wird, während Sie den DELETE-Befehl ausgeben, wird der Dienst zum Löschen markiert, er wird jedoch weiterhin ausgeführt, bis er beendet wird und alle geöffneten Handles geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="0c3c4-170">Wenn der Dienst nie beendet wird, wird der Dienst nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="0c3c4-171">Wenn Sie einen Dienst entfernen, wird die ausführbare Datei des dienstanders nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="0c3c4-172">Wenn Sie einen Dienst mithilfe von WMI entfernen, werden die zugehörigen Registrierungseinträge unter HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="0c3c4-173">Daher wird der Dienst nicht mehr installiert und ist nicht über das Dienste-Snap-in verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="0c3c4-174">Die ausführbare Datei wird von WMI jedoch nicht gelöscht, was bedeutet, dass Sie den Dienst problemlos neu installieren können.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="0c3c4-175">Zum Löschen der ausführbaren Datei müssen Sie den Pfadnamen abrufen und die Datei dann löschen.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="0c3c4-176">Wenn Sie einen Windows 2000-Basis Dienst (z. b. DHCP) mithilfe von WMI entfernen, werden die Registrierungseinträge für diesen Dienst gelöscht. die Verknüpfung wird jedoch nicht aus dem Menü "Verwaltung" entfernt, oder der Dienst wird aus dem Assistenten für Windows-Komponenten entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="0c3c4-177">Dies kann alle Benutzer verwirren, die versuchen, die Konfiguration des Computers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="0c3c4-178">Wenn Sie den DHCP-Dienst beispielsweise mithilfe eines WMI-Skripts entfernen, wird der DHCP-Dienst nicht mehr im Dienste-Snap-in aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="0c3c4-179">Eine nicht funktionsfähige Verknüpfung mit der DHCP-Konsole verbleibt jedoch im Menü "Verwaltung", und wenn Sie den Assistenten für Windows-Komponenten starten, bedeutet dies, dass der DHCP-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="0c3c4-180">Aus diesem Grund sollten Sie immer Sysocmgr.exe verwenden, um Windows 2000-Dienste Programm gesteuert zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="0c3c4-181">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c3c4-181">Examples</span></span>

<span data-ttu-id="0c3c4-182">Im folgenden VBScript-Codebeispiel wird beschrieben, wie ein Dienst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-182">The following VBScript code sample describes how to delete a service.</span></span>


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



<span data-ttu-id="0c3c4-183">Im folgenden perl-Codebeispiel wird beschrieben, wie ein Dienst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0c3c4-183">The following Perl code sample describes how to delete a service.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0c3c4-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c3c4-184">Requirements</span></span>



| <span data-ttu-id="0c3c4-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c3c4-185">Requirement</span></span> | <span data-ttu-id="0c3c4-186">Wert</span><span class="sxs-lookup"><span data-stu-id="0c3c4-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3c4-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c3c4-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3c4-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c3c4-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c3c4-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c3c4-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3c4-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c3c4-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c3c4-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c3c4-191">Namespace</span></span><br/>                | <span data-ttu-id="0c3c4-192">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0c3c4-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c3c4-193">MOF</span><span class="sxs-lookup"><span data-stu-id="0c3c4-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c3c4-194"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0c3c4-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c3c4-195">DLL</span><span class="sxs-lookup"><span data-stu-id="0c3c4-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c3c4-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c3c4-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c3c4-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c3c4-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c3c4-198">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c3c4-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c3c4-199">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="0c3c4-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="0c3c4-200">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="0c3c4-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

