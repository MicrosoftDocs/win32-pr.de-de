---
description: Versucht, den Dienst, auf den verwiesen wird, im angehaltenen Zustand zu platzieren.
ms.assetid: 57b8ccdd-056a-4bec-a0f8-ecebcf18039e
ms.tgt_platform: multiple
title: PauseService-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4828b81af5d6d543aaf16a34a08350f09078d623
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345461"
---
# <a name="pauseservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="c33f3-103">PauseService-Methode der Win32 \_ baseservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c33f3-103">PauseService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="c33f3-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode " **PauseService** " versucht, den referenzierten Dienst im angehaltenen Zustand zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="c33f3-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the paused state.</span></span>

<span data-ttu-id="c33f3-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c33f3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c33f3-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c33f3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c33f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c33f3-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="c33f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c33f3-108">Parameters</span></span>

<span data-ttu-id="c33f3-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c33f3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c33f3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c33f3-110">Return value</span></span>

<span data-ttu-id="c33f3-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c33f3-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c33f3-112">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="c33f3-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-113">0</span><span class="sxs-lookup"><span data-stu-id="c33f3-113">0</span></span>

<span data-ttu-id="c33f3-114">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c33f3-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-115">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="c33f3-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-116">1</span><span class="sxs-lookup"><span data-stu-id="c33f3-116">1</span></span>

<span data-ttu-id="c33f3-117">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-118">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="c33f3-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-119">2</span><span class="sxs-lookup"><span data-stu-id="c33f3-119">2</span></span>

<span data-ttu-id="c33f3-120">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c33f3-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-121">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="c33f3-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-122">3</span><span class="sxs-lookup"><span data-stu-id="c33f3-122">3</span></span>

<span data-ttu-id="c33f3-123">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c33f3-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-124">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-125">4</span><span class="sxs-lookup"><span data-stu-id="c33f3-125">4</span></span>

<span data-ttu-id="c33f3-126">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="c33f3-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-127">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-128">5</span><span class="sxs-lookup"><span data-stu-id="c33f3-128">5</span></span>

<span data-ttu-id="c33f3-129">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32 \_ baseservice**](win32-baseservice.md)[**State**](win32-baseservice.md) -Eigenschaft) gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="c33f3-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-130">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="c33f3-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-131">6</span><span class="sxs-lookup"><span data-stu-id="c33f3-131">6</span></span>

<span data-ttu-id="c33f3-132">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c33f3-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-133">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="c33f3-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-134">7</span><span class="sxs-lookup"><span data-stu-id="c33f3-134">7</span></span>

<span data-ttu-id="c33f3-135">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="c33f3-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-136">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-137">8</span><span class="sxs-lookup"><span data-stu-id="c33f3-137">8</span></span>

<span data-ttu-id="c33f3-138">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="c33f3-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-139">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="c33f3-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-140">9</span><span class="sxs-lookup"><span data-stu-id="c33f3-140">9</span></span>

<span data-ttu-id="c33f3-141">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c33f3-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-142">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-143">10</span><span class="sxs-lookup"><span data-stu-id="c33f3-143">10</span></span>

<span data-ttu-id="c33f3-144">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-145">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="c33f3-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-146">11</span><span class="sxs-lookup"><span data-stu-id="c33f3-146">11</span></span>

<span data-ttu-id="c33f3-147">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-148">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="c33f3-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-149">12</span><span class="sxs-lookup"><span data-stu-id="c33f3-149">12</span></span>

<span data-ttu-id="c33f3-150">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-151">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="c33f3-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-152">13</span><span class="sxs-lookup"><span data-stu-id="c33f3-152">13</span></span>

<span data-ttu-id="c33f3-153">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c33f3-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-154">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="c33f3-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-155">14</span><span class="sxs-lookup"><span data-stu-id="c33f3-155">14</span></span>

<span data-ttu-id="c33f3-156">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c33f3-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-157">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="c33f3-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-158">15</span><span class="sxs-lookup"><span data-stu-id="c33f3-158">15</span></span>

<span data-ttu-id="c33f3-159">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c33f3-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-160">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-161">16</span><span class="sxs-lookup"><span data-stu-id="c33f3-161">16</span></span>

<span data-ttu-id="c33f3-162">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-163">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="c33f3-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-164">17</span><span class="sxs-lookup"><span data-stu-id="c33f3-164">17</span></span>

<span data-ttu-id="c33f3-165">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="c33f3-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-166">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="c33f3-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-167">18</span><span class="sxs-lookup"><span data-stu-id="c33f3-167">18</span></span>

<span data-ttu-id="c33f3-168">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="c33f3-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-169">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="c33f3-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-170">19</span><span class="sxs-lookup"><span data-stu-id="c33f3-170">19</span></span>

<span data-ttu-id="c33f3-171">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-172">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="c33f3-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-173">20</span><span class="sxs-lookup"><span data-stu-id="c33f3-173">20</span></span>

<span data-ttu-id="c33f3-174">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c33f3-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-175">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-176">21</span><span class="sxs-lookup"><span data-stu-id="c33f3-176">21</span></span>

<span data-ttu-id="c33f3-177">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c33f3-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-178">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-179">22</span><span class="sxs-lookup"><span data-stu-id="c33f3-179">22</span></span>

<span data-ttu-id="c33f3-180">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c33f3-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-181">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c33f3-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-182">23</span><span class="sxs-lookup"><span data-stu-id="c33f3-182">23</span></span>

<span data-ttu-id="c33f3-183">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c33f3-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-184">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="c33f3-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-185">24</span><span class="sxs-lookup"><span data-stu-id="c33f3-185">24</span></span>

<span data-ttu-id="c33f3-186">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="c33f3-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c33f3-187">**Andere**</span><span class="sxs-lookup"><span data-stu-id="c33f3-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c33f3-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c33f3-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c33f3-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c33f3-189">Requirements</span></span>



| <span data-ttu-id="c33f3-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c33f3-190">Requirement</span></span> | <span data-ttu-id="c33f3-191">Wert</span><span class="sxs-lookup"><span data-stu-id="c33f3-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33f3-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c33f3-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c33f3-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c33f3-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c33f3-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c33f3-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c33f3-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c33f3-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c33f3-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="c33f3-196">Namespace</span></span><br/>                | <span data-ttu-id="c33f3-197">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c33f3-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c33f3-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c33f3-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c33f3-199"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c33f3-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c33f3-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c33f3-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33f3-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c33f3-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33f3-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c33f3-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="c33f3-203">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c33f3-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c33f3-204">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="c33f3-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

