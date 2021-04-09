---
description: Der Neustart&\# 8194; Die WMI-Klassenmethode fährt das Computersystem herunter und startet Sie neu.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Reboot-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958527"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="07a35-103">Reboot-Methode der Win32- \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="07a35-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="07a35-104">Beim **Neustart** der [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode wird das Computersystem heruntergefahren und dann neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="07a35-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="07a35-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="07a35-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07a35-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07a35-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07a35-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="07a35-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="07a35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="07a35-108">Parameters</span></span>

<span data-ttu-id="07a35-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="07a35-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07a35-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07a35-110">Return value</span></span>

<span data-ttu-id="07a35-111">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="07a35-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="07a35-112">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="07a35-112">Any other number indicates an error.</span></span> <span data-ttu-id="07a35-113">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="07a35-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="07a35-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="07a35-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="07a35-115">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="07a35-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07a35-116">**Sonstige** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="07a35-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="07a35-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07a35-117">Remarks</span></span>

<span data-ttu-id="07a35-118">Durch die Möglichkeit, einen Computerprogramm gesteuert neu zu starten, können Administratoren viele Computer Verwaltungsaufgaben Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="07a35-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="07a35-119">Wenn Sie z. b. ein Skript zum Installieren von Software erstellen oder eine Konfigurationsänderung vornehmen, für die ein Neustart eines Computers erforderlich ist, können Sie den Restart-Befehl in das Skript einschließen und den gesamten Vorgang Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="07a35-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="07a35-120">Die **Neustart** Methode kann zum Neustarten eines Computers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07a35-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="07a35-121">Wie die [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode erfordert die **Reboot** -Methode, dass der Benutzer, dessen Sicherheits Anmelde Informationen vom Skript verwendet werden, das Shutdown-Privileg besitzt.</span><span class="sxs-lookup"><span data-stu-id="07a35-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="07a35-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07a35-122">Examples</span></span>

<span data-ttu-id="07a35-123">Im folgenden VBScript-Codebeispiel wird die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="07a35-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="07a35-124">Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="07a35-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="07a35-125">Der folgende Perl-Code Ruft die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="07a35-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="07a35-126">Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="07a35-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="07a35-127">Das folgende VBScript Ruft die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse auf einem Remote System auf.</span><span class="sxs-lookup"><span data-stu-id="07a35-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="07a35-128">Geben Sie \_ den Remote System \_ Namen mit dem Namen des Remote Systems ein, das neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="07a35-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="07a35-129">Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die Neustart Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="07a35-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="07a35-130">der folgende perl Ruft die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse auf einem Remote System auf.</span><span class="sxs-lookup"><span data-stu-id="07a35-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="07a35-131">Geben Sie \_ den Remote System \_ Namen mit dem Namen des Remote Systems ein, das neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="07a35-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="07a35-132">Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die Neustart Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="07a35-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="07a35-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07a35-133">Requirements</span></span>



| <span data-ttu-id="07a35-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07a35-134">Requirement</span></span> | <span data-ttu-id="07a35-135">Wert</span><span class="sxs-lookup"><span data-stu-id="07a35-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a35-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07a35-136">Minimum supported client</span></span><br/> | <span data-ttu-id="07a35-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07a35-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07a35-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07a35-138">Minimum supported server</span></span><br/> | <span data-ttu-id="07a35-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a35-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07a35-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="07a35-140">Namespace</span></span><br/>                | <span data-ttu-id="07a35-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07a35-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07a35-142">MOF</span><span class="sxs-lookup"><span data-stu-id="07a35-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07a35-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="07a35-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07a35-144">DLL</span><span class="sxs-lookup"><span data-stu-id="07a35-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a35-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a35-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a35-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07a35-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="07a35-147">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07a35-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="07a35-148">**Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="07a35-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="07a35-149">**CIM \_ OperatingSystem. Shutdown-Methode**</span><span class="sxs-lookup"><span data-stu-id="07a35-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="07a35-150">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="07a35-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

