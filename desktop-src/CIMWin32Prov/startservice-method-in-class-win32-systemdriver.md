---
description: Versucht, den vom System Treiber verwalteten Dienst in seinen Startzustand zu versetzen.
ms.assetid: 3f9d29aa-b549-4a55-be9c-01fad4932fe6
ms.tgt_platform: multiple
title: Start Service-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c189d9b5f24a3ccc803a588abb94337ee65a1da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214164"
---
# <a name="startservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="59eae-103">Start Service-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="59eae-103">StartService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="59eae-104">Die **Start Service** -Methode versucht, den vom System Treiber verwalteten Dienst in den Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="59eae-104">The **StartService** method attempts to place the service managed by the system driver into its startup state.</span></span>

<span data-ttu-id="59eae-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="59eae-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59eae-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="59eae-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59eae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59eae-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="59eae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59eae-108">Parameters</span></span>

<span data-ttu-id="59eae-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="59eae-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59eae-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59eae-110">Return value</span></span>

<span data-ttu-id="59eae-111">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="59eae-111">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="59eae-112">**0**</span><span class="sxs-lookup"><span data-stu-id="59eae-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-113">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="59eae-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-114">**1**</span><span class="sxs-lookup"><span data-stu-id="59eae-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-115">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59eae-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-116">**2**</span><span class="sxs-lookup"><span data-stu-id="59eae-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-117">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="59eae-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-118">**3**</span><span class="sxs-lookup"><span data-stu-id="59eae-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-119">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="59eae-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-120">**4**</span><span class="sxs-lookup"><span data-stu-id="59eae-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-121">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="59eae-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-122">**5**</span><span class="sxs-lookup"><span data-stu-id="59eae-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-123">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="59eae-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-124">**6**</span><span class="sxs-lookup"><span data-stu-id="59eae-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-125">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="59eae-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-126">**7**</span><span class="sxs-lookup"><span data-stu-id="59eae-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-127">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="59eae-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-128">**8**</span><span class="sxs-lookup"><span data-stu-id="59eae-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-129">Beim Starten des Diensts ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="59eae-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-130">**9**</span><span class="sxs-lookup"><span data-stu-id="59eae-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-131">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="59eae-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-132">**10**</span><span class="sxs-lookup"><span data-stu-id="59eae-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-133">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59eae-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-134">**11**</span><span class="sxs-lookup"><span data-stu-id="59eae-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-135">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="59eae-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-136">**12**</span><span class="sxs-lookup"><span data-stu-id="59eae-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-137">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="59eae-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-138">**13**</span><span class="sxs-lookup"><span data-stu-id="59eae-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-139">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="59eae-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-140">**14**</span><span class="sxs-lookup"><span data-stu-id="59eae-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-141">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="59eae-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-142">**15**</span><span class="sxs-lookup"><span data-stu-id="59eae-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-143">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="59eae-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-144">**16**</span><span class="sxs-lookup"><span data-stu-id="59eae-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-145">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="59eae-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-146">**17**</span><span class="sxs-lookup"><span data-stu-id="59eae-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-147">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="59eae-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-148">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="59eae-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-149">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="59eae-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-150">**19**</span><span class="sxs-lookup"><span data-stu-id="59eae-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-151">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59eae-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-152">**20**</span><span class="sxs-lookup"><span data-stu-id="59eae-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-153">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="59eae-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-154">**21**</span><span class="sxs-lookup"><span data-stu-id="59eae-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-155">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="59eae-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-156">**22**</span><span class="sxs-lookup"><span data-stu-id="59eae-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-157">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="59eae-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-158">**23**</span><span class="sxs-lookup"><span data-stu-id="59eae-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-159">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="59eae-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-160">**24**</span><span class="sxs-lookup"><span data-stu-id="59eae-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="59eae-161">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="59eae-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="59eae-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59eae-162">Examples</span></span>

<span data-ttu-id="59eae-163">Der folgende PowerShell-Code startet den Dienst "Microsoft USB Printer Class".</span><span class="sxs-lookup"><span data-stu-id="59eae-163">The following PowerShell code starts the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StartService()
"Start Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="59eae-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59eae-164">Requirements</span></span>



| <span data-ttu-id="59eae-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59eae-165">Requirement</span></span> | <span data-ttu-id="59eae-166">Wert</span><span class="sxs-lookup"><span data-stu-id="59eae-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59eae-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59eae-167">Minimum supported client</span></span><br/> | <span data-ttu-id="59eae-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59eae-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59eae-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59eae-169">Minimum supported server</span></span><br/> | <span data-ttu-id="59eae-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59eae-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59eae-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="59eae-171">Namespace</span></span><br/>                | <span data-ttu-id="59eae-172">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="59eae-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59eae-173">MOF</span><span class="sxs-lookup"><span data-stu-id="59eae-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59eae-174"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59eae-175">DLL</span><span class="sxs-lookup"><span data-stu-id="59eae-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59eae-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eae-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59eae-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="59eae-178">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59eae-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="59eae-179">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="59eae-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

