---
description: Das Herunterfahren&\# 8194; Die WMI-Klassenmethode entlädt Programme und DLLs, bis der Computer sicher ausgeschaltet wird.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Shutdown-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483966"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="e789e-103">Shutdown-Methode der Win32- \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="e789e-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="e789e-104">Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode für das Herunterfahren entlädt Programme und DLLs, bis Sie den Computer sicher ausschalten können.</span><span class="sxs-lookup"><span data-stu-id="e789e-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="e789e-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e789e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e789e-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e789e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e789e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e789e-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="e789e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e789e-108">Parameters</span></span>

<span data-ttu-id="e789e-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e789e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e789e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e789e-110">Return value</span></span>

<span data-ttu-id="e789e-111">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e789e-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="e789e-112">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e789e-112">Any other number indicates an error.</span></span> <span data-ttu-id="e789e-113">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e789e-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e789e-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e789e-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e789e-115">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="e789e-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e789e-116">**Sonstige** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e789e-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e789e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e789e-117">Remarks</span></span>

<span data-ttu-id="e789e-118">Computer müssen gelegentlich aus dem Netzwerk entfernt werden, möglicherweise für eine geplante Wartung, weil der Computer nicht ordnungsgemäß funktioniert, oder um einen Konfigurationsprozess abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e789e-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="e789e-119">Wenn ein DHCP-Server z. b. fehlerhafte IP-Adressen ausgibt, sollten Sie den Computer Herunterfahren, bis ein Dienst Techniker zur Behebung des Problems weitergeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e789e-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="e789e-120">Wenn Sie vermuten, dass ein Sicherheits Verstoß aufgetreten ist, müssen Sie möglicherweise bestimmte Server herunterfahren, um sicherzustellen, dass auf Sie nicht zugegriffen werden kann, bis das Sicherheitsproblem behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="e789e-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="e789e-121">Einige Konfigurations Vorgänge (z. b. das Ändern eines Computer namens) erfordern, dass Sie den Computer neu starten, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="e789e-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="e789e-122">Mit dieser Methode wird der Computer nach Möglichkeit sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e789e-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="e789e-123">Das System beendet alle laufenden Prozesse, leert alle Datei Puffer auf den Datenträger und schaltet dann das System herunter.</span><span class="sxs-lookup"><span data-stu-id="e789e-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="e789e-124">Der aufrufende Prozess muss über die Berechtigung für das Herunterfahren des **\_ \_ namens** verfügen, wie im folgenden Beispiel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e789e-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="e789e-125">Weitere Informationen zum Festlegen einer Berechtigung finden Sie unter [Ausführen von privilegierten Vorgängen](/windows/desktop/WmiSdk/executing-privileged-operations) und [Ausführen von privilegierten Vorgängen mit VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="e789e-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="e789e-126">Weitere Optionen für das Herunterfahren, z. b. ein Abmelde-oder Erzwungenes Herunterfahren, finden Sie unter [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e789e-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="e789e-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e789e-127">Examples</span></span>

<span data-ttu-id="e789e-128">Mit dem folgenden VBScript-Code wird der lokale Computer heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e789e-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="e789e-129">Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="e789e-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="e789e-130">Der folgende Perl-Code schaltet den lokalen Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="e789e-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="e789e-131">Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="e789e-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



<span data-ttu-id="e789e-132">Mit dem folgenden VBScript-Code wird der angegebene Remote Computer heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e789e-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="e789e-133">Geben Sie den *Remote \_ System \_ Namen* mit dem Namen des Remote Systems ein, das heruntergefahren werden soll.</span><span class="sxs-lookup"><span data-stu-id="e789e-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="e789e-134">Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die **Shutdown** -Methode erfolgreich aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="e789e-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="e789e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e789e-135">Requirements</span></span>



| <span data-ttu-id="e789e-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e789e-136">Requirement</span></span> | <span data-ttu-id="e789e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="e789e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e789e-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e789e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e789e-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e789e-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e789e-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e789e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e789e-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e789e-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e789e-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="e789e-142">Namespace</span></span><br/>                | <span data-ttu-id="e789e-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e789e-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e789e-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e789e-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e789e-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e789e-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e789e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e789e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e789e-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e789e-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e789e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e789e-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="e789e-149">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e789e-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e789e-150">**Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e789e-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="e789e-151">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e789e-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="e789e-152">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="e789e-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

