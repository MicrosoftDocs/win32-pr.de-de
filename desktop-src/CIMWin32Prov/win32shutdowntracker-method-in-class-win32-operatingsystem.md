---
description: Die Win32ShutdownTracker-Methode bietet die gleichen Optionen für das Herunterfahren, die von der Win32Shutdown-Methode im Win32- \_ OperatingSystem unterstützt werden, Sie ermöglicht Ihnen aber auch das Angeben von Kommentaren, den Grund für das Herunterfahren oder ein Timeout.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Win32ShutdownTracker-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126073"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="65fe7-103">Win32ShutdownTracker-Methode der Win32 \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="65fe7-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="65fe7-104">Die **Win32ShutdownTracker** -Methode bietet die gleichen Optionen für das Herunterfahren, die von der [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode im [**Win32- \_ OperatingSystem**](win32-operatingsystem.md)unterstützt werden, Sie ermöglicht Ihnen aber auch das Angeben von Kommentaren, den Grund für das Herunterfahren oder ein Timeout.</span><span class="sxs-lookup"><span data-stu-id="65fe7-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fe7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65fe7-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="65fe7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65fe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65fe7-107">*Timeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65fe7-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-108">Zeit in Sekunden, bevor das Herunterfahren stattfindet.</span><span class="sxs-lookup"><span data-stu-id="65fe7-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="65fe7-109">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="65fe7-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-110">*Kommentar* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65fe7-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-111">Die Meldung, die im Dialogfeld zum Herunterfahren angezeigt wird, das auch als Kommentar im Ereignisprotokoll Eintrag gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="65fe7-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-112">*Reasoncode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65fe7-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-113">Grund für das Initiieren des herunter Fahrens.</span><span class="sxs-lookup"><span data-stu-id="65fe7-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="65fe7-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-115">Bitzugeordneter Satz von Flags, um den Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="65fe7-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="65fe7-116">Fügen Sie dem Befehls Wert das Force-Flag (4) hinzu, um einen Befehl zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="65fe7-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="65fe7-117">Durch die Verwendung von Force in Verbindung mit dem Herunterfahren oder Neustart auf einem Remote Computer wird sofort alles heruntergefahren (einschließlich WMI, com usw.) oder der Remote Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="65fe7-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="65fe7-118">Dies führt zu einem unbestimmten Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="65fe7-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="65fe7-119">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="65fe7-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-120">Abmelden</span><span class="sxs-lookup"><span data-stu-id="65fe7-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="65fe7-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-122">Erzwungene Protokollierung (0 + 4)</span><span class="sxs-lookup"><span data-stu-id="65fe7-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="65fe7-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-124">Shutdown</span><span class="sxs-lookup"><span data-stu-id="65fe7-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="65fe7-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-126">Erzwungenes Herunterfahren (1 + 4)</span><span class="sxs-lookup"><span data-stu-id="65fe7-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="65fe7-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-128">Reboot</span><span class="sxs-lookup"><span data-stu-id="65fe7-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-129">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="65fe7-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-130">Erzwungener Neustart (2 + 4)</span><span class="sxs-lookup"><span data-stu-id="65fe7-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="65fe7-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-132">Ausschalten</span><span class="sxs-lookup"><span data-stu-id="65fe7-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="65fe7-133">12 (0xc)</span><span class="sxs-lookup"><span data-stu-id="65fe7-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="65fe7-134">Erzwungene Stromversorgung (8 + 4)</span><span class="sxs-lookup"><span data-stu-id="65fe7-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65fe7-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65fe7-135">Return value</span></span>

<span data-ttu-id="65fe7-136">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="65fe7-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="65fe7-137">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="65fe7-137">Any other number indicates an error.</span></span> <span data-ttu-id="65fe7-138">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](../wmisdk/wmi-error-constants.md) oder [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="65fe7-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="65fe7-139">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="65fe7-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="65fe7-140">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="65fe7-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="65fe7-141">**Sonstige** (1 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="65fe7-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="65fe7-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65fe7-142">Remarks</span></span>

<span data-ttu-id="65fe7-143">Der Aufrufprozess muss über die Berechtigung für das Herunterfahren des **\_ \_ namens** verfügen.</span><span class="sxs-lookup"><span data-stu-id="65fe7-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="65fe7-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65fe7-144">Examples</span></span>

<span data-ttu-id="65fe7-145">Im folgenden VBScript-Codebeispiel wird beschrieben, wie **Win32ShutdownTracker** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="65fe7-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="65fe7-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65fe7-146">Requirements</span></span>



| <span data-ttu-id="65fe7-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65fe7-147">Requirement</span></span> | <span data-ttu-id="65fe7-148">Wert</span><span class="sxs-lookup"><span data-stu-id="65fe7-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65fe7-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65fe7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="65fe7-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65fe7-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65fe7-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65fe7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="65fe7-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65fe7-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65fe7-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="65fe7-153">Namespace</span></span><br/>                | <span data-ttu-id="65fe7-154">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65fe7-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65fe7-155">MOF</span><span class="sxs-lookup"><span data-stu-id="65fe7-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65fe7-156"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="65fe7-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65fe7-157">DLL</span><span class="sxs-lookup"><span data-stu-id="65fe7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65fe7-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65fe7-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65fe7-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65fe7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fe7-160">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="65fe7-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="65fe7-161">**Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="65fe7-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="65fe7-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="65fe7-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
