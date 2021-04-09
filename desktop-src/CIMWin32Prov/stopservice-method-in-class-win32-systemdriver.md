---
description: Versetzt den Dienst, der durch das Win32 systemdriver-Objekt dargestellt wird, \_ in den Zustand "beendet".
ms.assetid: 0fa8ef44-39eb-448e-8d33-38a5af9a0c13
ms.tgt_platform: multiple
title: Stop Service-Methode der Win32_SystemDriver-Klasse (sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb45a414ea9cc7198487dbb61d122722816f4728
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958378"
---
# <a name="stopservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="e7e8f-103">Stop Service-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="e7e8f-103">StopService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="e7e8f-104">Die **StopService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode platziert den Dienst, der durch das [**Win32 \_ systemdriver**](win32-systemdriver.md) -Objekt dargestellt wird, im beendeten Zustand.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_SystemDriver**](win32-systemdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="e7e8f-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e7e8f-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e7e8f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7e8f-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="e7e8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7e8f-108">Parameters</span></span>

<span data-ttu-id="e7e8f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7e8f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7e8f-110">Return value</span></span>

<span data-ttu-id="e7e8f-111">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich beendet wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-111">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e7e8f-112">**0**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-113">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-114">**1**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-115">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-116">**2**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-117">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-118">**3**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-119">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-120">**4**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-121">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-122">**5**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-123">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-124">**6**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-125">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-126">**7**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-127">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-128">**8**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-129">Beim Starten des Diensts ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-130">**9**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-131">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-132">**10**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-133">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-134">**11**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-135">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-136">**12**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-137">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-138">**13**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-139">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-140">**14**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-141">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-142">**15**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-143">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-144">**16**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-145">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-146">**17**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-147">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-148">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-149">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-150">**19**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-151">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-152">**20**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-153">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-154">**21**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-155">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-156">**22**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-157">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-158">**23**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-159">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8f-160">**24**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8f-161">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="e7e8f-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e7e8f-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7e8f-162">Examples</span></span>

<span data-ttu-id="e7e8f-163">Der folgende PowerShell-Code beendet den Dienst "Microsoft USB Printer Class".</span><span class="sxs-lookup"><span data-stu-id="e7e8f-163">The following PowerShell code stops the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StopService()
"Stop Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="e7e8f-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7e8f-164">Requirements</span></span>



| <span data-ttu-id="e7e8f-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7e8f-165">Requirement</span></span> | <span data-ttu-id="e7e8f-166">Wert</span><span class="sxs-lookup"><span data-stu-id="e7e8f-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e8f-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7e8f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e8f-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7e8f-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7e8f-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7e8f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e8f-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e8f-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7e8f-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7e8f-171">Namespace</span></span><br/>                | <span data-ttu-id="e7e8f-172">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7e8f-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7e8f-173">Header</span><span class="sxs-lookup"><span data-stu-id="e7e8f-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7e8f-174"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e8f-174"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="e7e8f-175">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e8f-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e8f-176"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e7e8f-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e8f-177">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e8f-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e8f-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e8f-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e8f-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7e8f-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7e8f-180">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7e8f-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e7e8f-181">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="e7e8f-181">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

