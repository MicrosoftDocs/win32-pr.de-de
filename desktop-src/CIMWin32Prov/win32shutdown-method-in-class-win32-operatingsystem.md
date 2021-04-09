---
description: Die Win32Shutdown-&\# 8194; Die WMI-Klassenmethode bietet alle Optionen für das Herunterfahren, die von Win32-Betriebssystemen unterstützt werden. Hierzu gehören das Abmelden, das Herunterfahren, das Neustarten und das Erzwingen einer Abmeldung, eines herunter Fahrens oder eines Neustarts.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Win32Shutdown-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861571"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="64590-104">Win32Shutdown-Methode der Win32 \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="64590-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="64590-105">Die **Win32Shutdown** -   [WMI-Klassen](../wmisdk/retrieving-a-class.md) Methode bietet alle Optionen für das Herunterfahren, die von Win32-Betriebssystemen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="64590-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="64590-106">Hierzu gehören das Abmelden, das Herunterfahren, das Neustarten und das Erzwingen einer Abmeldung, eines herunter Fahrens oder eines Neustarts.</span><span class="sxs-lookup"><span data-stu-id="64590-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="64590-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="64590-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="64590-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](../wmisdk/calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="64590-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64590-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="64590-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="64590-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64590-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64590-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="64590-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64590-112">Bitzugeordneter Satz von Flags, um den Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="64590-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="64590-113">Fügen Sie dem Befehls Wert das Force-Flag (4) hinzu, um einen Befehl zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="64590-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="64590-114">Durch die Verwendung von Force in Verbindung mit dem Herunterfahren oder Neustart auf einem Remote Computer wird sofort alles heruntergefahren (einschließlich WMI, com usw.) oder der Remote Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="64590-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="64590-115">Dies führt zu einem unbestimmten Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="64590-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="64590-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="64590-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="64590-117">**Abmelden** : protokolliert den Benutzer vom Computer.</span><span class="sxs-lookup"><span data-stu-id="64590-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="64590-118">Beim Abmelden werden alle Prozesse angehalten, die dem Sicherheitskontext des Prozesses zugeordnet sind, der die Funktion Exit aufgerufen hat, der aktuelle Benutzer wird vom System protokolliert und das Anmelde Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="64590-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="64590-119">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="64590-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="64590-120">**Erzwungene Abmeldung (0 + 4)** : der Benutzer wird vom Computer sofort protokolliert, und die Anwendung wird nicht benachrichtigt, dass die Anmelde Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="64590-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="64590-121">Dies kann zu einem Datenverlust führen.</span><span class="sxs-lookup"><span data-stu-id="64590-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="64590-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="64590-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="64590-123">**Herunter** fahren: der Computer wird an einen Punkt heruntergefahren, an dem die Stromversorgung deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="64590-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="64590-124">(Alle Datei Puffer werden auf den Datenträger geleert, und alle ausgelaufenden Prozesse werden beendet.) Benutzern wird die Meldung angezeigt. `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="64590-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="64590-125">Während des herunter Fahrens sendet das System eine Meldung an jede laufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="64590-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="64590-126">Die Anwendungen führen bei der Verarbeitung der Nachricht alle Bereinigungs Vorgänge aus und geben true zurück, um anzugeben, dass Sie beendet werden können.</span><span class="sxs-lookup"><span data-stu-id="64590-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="64590-127">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="64590-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="64590-128">**Erzwungenes Herunterfahren (1 + 4)** : fährt den Computer an einen Punkt herunter, an dem die Stromversorgung deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="64590-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="64590-129">(Alle Datei Puffer werden auf den Datenträger geleert, und alle ausgelaufenden Prozesse werden beendet.) Benutzern wird die Meldung angezeigt.` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="64590-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="64590-130">Wenn das erzwungene Herunterfahren verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="64590-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="64590-131">Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remote Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="64590-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="64590-132">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="64590-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="64590-133">**Neustart** : der Computer wird heruntergefahren, und der Computer wird neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="64590-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="64590-134">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="64590-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="64590-135">**Erzwungener Neustart (2 + 4)** : der Computer wird heruntergefahren, und der Computer wird neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="64590-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="64590-136">Wenn der erzwungene Neustart Ansatz verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="64590-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="64590-137">Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remote Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="64590-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="64590-138">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="64590-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="64590-139">**Ausschalten** : schaltet den Computer herunter und schaltet die Stromversorgung aus (sofern vom betreffenden Computer unterstützt).</span><span class="sxs-lookup"><span data-stu-id="64590-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="64590-140">12 (0xc)</span><span class="sxs-lookup"><span data-stu-id="64590-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="64590-141">**Erzwungene Stromversorgung (8 + 4)** : der Computer wird heruntergefahren, und die Leistung wird ausgeschaltet (sofern vom betreffenden Computer unterstützt).</span><span class="sxs-lookup"><span data-stu-id="64590-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="64590-142">Wenn die erzwungene Stromversorgung verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="64590-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="64590-143">Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remote Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="64590-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="64590-144">*Reserviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64590-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64590-145">Eine Möglichkeit, **Win32Shutdown** zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="64590-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="64590-146">Derzeit wird der *reservierte* Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="64590-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64590-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64590-147">Return value</span></span>

<span data-ttu-id="64590-148">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64590-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="64590-149">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="64590-149">Any other number indicates an error.</span></span> <span data-ttu-id="64590-150">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](../wmisdk/wmi-error-constants.md) oder [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="64590-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="64590-151">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="64590-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="64590-152">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="64590-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64590-153">**Sonstige** (1 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="64590-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="64590-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64590-154">Remarks</span></span>

<span data-ttu-id="64590-155">Zur effizienteren Verwaltung von Computern in einer Organisation benötigen Administratoren die Möglichkeit, einen Computer Remote herunterzufahren oder neu zu starten oder einen Benutzer Remote abzumelden.</span><span class="sxs-lookup"><span data-stu-id="64590-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="64590-156">Durch die Möglichkeit, diese Aufgaben auszuführen, können Administratoren Software installieren, Computereinstellungen neu konfigurieren, Computer aus dem Netzwerk entfernen und andere Tasks ausführen, ohne jeden Computer manuell herunterfahren oder neu starten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="64590-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="64590-157">Wenn Sie z. b. ein Netzwerk Upgrade durchführen möchten, müssen Sie möglicherweise alle Computer Herunterfahren, die in einem bestimmten Netzwerksegment ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64590-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="64590-158">Um ein Gruppenrichtlinie Upgrade zu erzwingen, müssen Sie Benutzer auf ihren Computern protokollieren.</span><span class="sxs-lookup"><span data-stu-id="64590-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="64590-159">Wenn ein Computervirus an einer beliebigen Stelle in Ihrer Organisation vorhanden ist, empfiehlt es sich, so viele Computer wie möglich herunterzufahren, bevor der Virus verteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="64590-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="64590-160">Die Möglichkeit, Computer herunterzufahren und neu zu starten und Benutzerprogramm gesteuert anstelle von manuell abzumelden, kann ein enormer Zeitersparnis sein.</span><span class="sxs-lookup"><span data-stu-id="64590-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="64590-161">Der Aufrufprozess muss über die Berechtigung für das Herunterfahren des **\_ \_ namens** verfügen.</span><span class="sxs-lookup"><span data-stu-id="64590-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="64590-162">Die [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) -Methode bietet denselben Satz von Optionen für das Herunterfahren, die von der **Win32Shutdown** -Methode im [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) unterstützt werden. Sie ermöglicht Ihnen aber auch das Angeben von Kommentaren, den Grund für das Herunterfahren oder ein Timeout.</span><span class="sxs-lookup"><span data-stu-id="64590-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="64590-163">Die Win32Shutdown-Methode verfügt über keinen Parameter zum Sperren einer Arbeitsstation, sodass der Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="64590-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="64590-164">Arbeitsstationen können jedoch mit dem folgenden Befehl über die Befehlszeile gesperrt werden:</span><span class="sxs-lookup"><span data-stu-id="64590-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="64590-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64590-165">Examples</span></span>

<span data-ttu-id="64590-166">Das VBScript-Beispiel zum [Abmelden, Neustarten oder Herunterfahren von mehreren Computern](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) in der TechNet Gallery verwendet Win32Shutdown, um die im Server Array aufgeführten Computer abzumelden, herunterzufahren, neu zu starten oder auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="64590-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="64590-167">Das [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell-Beispiel in der TechNet Gallery enthält eine Methode, mit der Win32Shutdown auf einem Remote Computer aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="64590-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="64590-168">Im folgenden PowerShell-Beispiel wird die Win32Shutdown-Methode verwendet, um den angegebenen Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="64590-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="64590-169">Im folgenden PowerShell-Codebeispiel wird das enableallprivileges-Cmdlet aus dem Get-WMIObject-Cmdlet verwendet, um die richtigen Privilegien zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="64590-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="64590-170">Der folgende VB.NET-Beispielcode verwendet die Shutdown-Methode, um ein System neu zu starten oder abzumelden.</span><span class="sxs-lookup"><span data-stu-id="64590-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="64590-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64590-171">Requirements</span></span>



| <span data-ttu-id="64590-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64590-172">Requirement</span></span> | <span data-ttu-id="64590-173">Wert</span><span class="sxs-lookup"><span data-stu-id="64590-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64590-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64590-174">Minimum supported client</span></span><br/> | <span data-ttu-id="64590-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64590-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64590-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64590-176">Minimum supported server</span></span><br/> | <span data-ttu-id="64590-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64590-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64590-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="64590-178">Namespace</span></span><br/>                | <span data-ttu-id="64590-179">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64590-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64590-180">MOF</span><span class="sxs-lookup"><span data-stu-id="64590-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64590-181"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="64590-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64590-182">DLL</span><span class="sxs-lookup"><span data-stu-id="64590-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64590-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64590-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64590-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64590-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64590-185">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="64590-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="64590-186">**Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="64590-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="64590-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="64590-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="64590-188">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="64590-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="64590-189">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="64590-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
