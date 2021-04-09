---
description: Versucht, den vom System Treiber verwalteten Dienst in den Status "wieder aufgenommen" zu versetzen.
ms.assetid: 16bacf06-4236-4d58-9b09-cb86bb73d78a
ms.tgt_platform: multiple
title: ResumeService-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d326fcd0a3bc9801f5e214cdc8740170cf1f1cf8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958235"
---
# <a name="resumeservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="f31fb-103">ResumeService-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="f31fb-103">ResumeService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="f31fb-104">Die **ResumeService** -Methode der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) versucht, den vom System Treiber verwalteten Dienst in den Status "fortgesetzt" zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="f31fb-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service managed by the system driver in the resumed state.</span></span>

<span data-ttu-id="f31fb-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f31fb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f31fb-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f31fb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f31fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f31fb-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="f31fb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f31fb-108">Parameters</span></span>

<span data-ttu-id="f31fb-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f31fb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f31fb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f31fb-110">Return value</span></span>

<span data-ttu-id="f31fb-111">Gibt einen Wert von 0 (null) zurück, wenn die **ResumeService** -Anforderung akzeptiert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="f31fb-111">Returns a value of 0 (zero) if the **ResumeService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f31fb-112">**0**</span><span class="sxs-lookup"><span data-stu-id="f31fb-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-113">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f31fb-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-114">**1**</span><span class="sxs-lookup"><span data-stu-id="f31fb-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-115">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-116">**2**</span><span class="sxs-lookup"><span data-stu-id="f31fb-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-117">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="f31fb-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-118">**3**</span><span class="sxs-lookup"><span data-stu-id="f31fb-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-119">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="f31fb-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-120">**4**</span><span class="sxs-lookup"><span data-stu-id="f31fb-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-121">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="f31fb-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-122">**5**</span><span class="sxs-lookup"><span data-stu-id="f31fb-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-123">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="f31fb-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-124">**6**</span><span class="sxs-lookup"><span data-stu-id="f31fb-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-125">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="f31fb-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-126">**7**</span><span class="sxs-lookup"><span data-stu-id="f31fb-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-127">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="f31fb-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-128">**8**</span><span class="sxs-lookup"><span data-stu-id="f31fb-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-129">Beim Starten des Diensts ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f31fb-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-130">**9**</span><span class="sxs-lookup"><span data-stu-id="f31fb-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-131">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f31fb-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-132">**10**</span><span class="sxs-lookup"><span data-stu-id="f31fb-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-133">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-134">**11**</span><span class="sxs-lookup"><span data-stu-id="f31fb-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-135">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-136">**12**</span><span class="sxs-lookup"><span data-stu-id="f31fb-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-137">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-138">**13**</span><span class="sxs-lookup"><span data-stu-id="f31fb-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-139">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="f31fb-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-140">**14**</span><span class="sxs-lookup"><span data-stu-id="f31fb-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-141">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f31fb-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-142">**15**</span><span class="sxs-lookup"><span data-stu-id="f31fb-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-143">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="f31fb-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-144">**16**</span><span class="sxs-lookup"><span data-stu-id="f31fb-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-145">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-146">**17**</span><span class="sxs-lookup"><span data-stu-id="f31fb-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-147">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="f31fb-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-148">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="f31fb-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-149">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="f31fb-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-150">**19**</span><span class="sxs-lookup"><span data-stu-id="f31fb-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-151">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-152">**20**</span><span class="sxs-lookup"><span data-stu-id="f31fb-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-153">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f31fb-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-154">**21**</span><span class="sxs-lookup"><span data-stu-id="f31fb-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-155">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f31fb-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-156">**22**</span><span class="sxs-lookup"><span data-stu-id="f31fb-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-157">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f31fb-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-158">**23**</span><span class="sxs-lookup"><span data-stu-id="f31fb-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-159">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f31fb-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f31fb-160">**24**</span><span class="sxs-lookup"><span data-stu-id="f31fb-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f31fb-161">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="f31fb-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f31fb-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f31fb-162">Examples</span></span>

<span data-ttu-id="f31fb-163">Der folgende PowerShell-Code versucht, den Dienst "Microsoft USB Printer Class" fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f31fb-163">The following PowerShell code attempts to resume the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.ResumeService()
"Resume Service Called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="f31fb-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f31fb-164">Requirements</span></span>



| <span data-ttu-id="f31fb-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f31fb-165">Requirement</span></span> | <span data-ttu-id="f31fb-166">Wert</span><span class="sxs-lookup"><span data-stu-id="f31fb-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31fb-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f31fb-167">Minimum supported client</span></span><br/> | <span data-ttu-id="f31fb-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f31fb-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f31fb-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f31fb-169">Minimum supported server</span></span><br/> | <span data-ttu-id="f31fb-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f31fb-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f31fb-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="f31fb-171">Namespace</span></span><br/>                | <span data-ttu-id="f31fb-172">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f31fb-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f31fb-173">MOF</span><span class="sxs-lookup"><span data-stu-id="f31fb-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f31fb-174"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f31fb-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f31fb-175">DLL</span><span class="sxs-lookup"><span data-stu-id="f31fb-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f31fb-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31fb-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31fb-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f31fb-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="f31fb-178">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f31fb-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f31fb-179">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="f31fb-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

