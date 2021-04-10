---
description: Ändert den Start Modus eines Win32- \_ Dienstanbieter.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: ChangeStartMode-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041417"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c4cad-103">ChangeStartMode-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="c4cad-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c4cad-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **ChangeStartMode** ändert den Start Modus eines [**Win32- \_ Dienstanbieter**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="c4cad-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="c4cad-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4cad-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c4cad-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c4cad-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4cad-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="c4cad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4cad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4cad-109">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4cad-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-110">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c4cad-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="c4cad-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="c4cad-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="c4cad-112">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="c4cad-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="c4cad-113">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="c4cad-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="c4cad-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span><span class="sxs-lookup"><span data-stu-id="c4cad-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="c4cad-115">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="c4cad-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c4cad-116">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="c4cad-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="c4cad-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="c4cad-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="c4cad-118">Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c4cad-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="c4cad-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="c4cad-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="c4cad-120">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="c4cad-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c4cad-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="c4cad-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="c4cad-122">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4cad-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4cad-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4cad-123">Return value</span></span>

<span data-ttu-id="c4cad-124">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c4cad-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="c4cad-125">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c4cad-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c4cad-126">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c4cad-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c4cad-127">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="c4cad-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-128">0</span><span class="sxs-lookup"><span data-stu-id="c4cad-128">0</span></span>

<span data-ttu-id="c4cad-129">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c4cad-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-130">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="c4cad-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-131">1</span><span class="sxs-lookup"><span data-stu-id="c4cad-131">1</span></span>

<span data-ttu-id="c4cad-132">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-133">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="c4cad-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-134">2</span><span class="sxs-lookup"><span data-stu-id="c4cad-134">2</span></span>

<span data-ttu-id="c4cad-135">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c4cad-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-136">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="c4cad-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-137">3</span><span class="sxs-lookup"><span data-stu-id="c4cad-137">3</span></span>

<span data-ttu-id="c4cad-138">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c4cad-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-139">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-140">4</span><span class="sxs-lookup"><span data-stu-id="c4cad-140">4</span></span>

<span data-ttu-id="c4cad-141">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="c4cad-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-142">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-143">5</span><span class="sxs-lookup"><span data-stu-id="c4cad-143">5</span></span>

<span data-ttu-id="c4cad-144">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="c4cad-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-145">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="c4cad-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-146">6</span><span class="sxs-lookup"><span data-stu-id="c4cad-146">6</span></span>

<span data-ttu-id="c4cad-147">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c4cad-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-148">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="c4cad-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-149">7</span><span class="sxs-lookup"><span data-stu-id="c4cad-149">7</span></span>

<span data-ttu-id="c4cad-150">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="c4cad-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-151">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-152">8</span><span class="sxs-lookup"><span data-stu-id="c4cad-152">8</span></span>

<span data-ttu-id="c4cad-153">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c4cad-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-154">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="c4cad-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-155">9</span><span class="sxs-lookup"><span data-stu-id="c4cad-155">9</span></span>

<span data-ttu-id="c4cad-156">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c4cad-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-157">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-158">10</span><span class="sxs-lookup"><span data-stu-id="c4cad-158">10</span></span>

<span data-ttu-id="c4cad-159">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-160">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="c4cad-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-161">11</span><span class="sxs-lookup"><span data-stu-id="c4cad-161">11</span></span>

<span data-ttu-id="c4cad-162">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-163">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="c4cad-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-164">12</span><span class="sxs-lookup"><span data-stu-id="c4cad-164">12</span></span>

<span data-ttu-id="c4cad-165">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-166">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="c4cad-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-167">13</span><span class="sxs-lookup"><span data-stu-id="c4cad-167">13</span></span>

<span data-ttu-id="c4cad-168">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cad-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-169">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="c4cad-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-170">14</span><span class="sxs-lookup"><span data-stu-id="c4cad-170">14</span></span>

<span data-ttu-id="c4cad-171">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4cad-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-172">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="c4cad-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-173">15</span><span class="sxs-lookup"><span data-stu-id="c4cad-173">15</span></span>

<span data-ttu-id="c4cad-174">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c4cad-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-175">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-176">16</span><span class="sxs-lookup"><span data-stu-id="c4cad-176">16</span></span>

<span data-ttu-id="c4cad-177">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-178">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="c4cad-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-179">17</span><span class="sxs-lookup"><span data-stu-id="c4cad-179">17</span></span>

<span data-ttu-id="c4cad-180">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="c4cad-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-181">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="c4cad-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-182">18</span><span class="sxs-lookup"><span data-stu-id="c4cad-182">18</span></span>

<span data-ttu-id="c4cad-183">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c4cad-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-184">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="c4cad-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-185">19</span><span class="sxs-lookup"><span data-stu-id="c4cad-185">19</span></span>

<span data-ttu-id="c4cad-186">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-187">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="c4cad-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-188">20</span><span class="sxs-lookup"><span data-stu-id="c4cad-188">20</span></span>

<span data-ttu-id="c4cad-189">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c4cad-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-190">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-191">21</span><span class="sxs-lookup"><span data-stu-id="c4cad-191">21</span></span>

<span data-ttu-id="c4cad-192">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c4cad-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-193">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-194">22</span><span class="sxs-lookup"><span data-stu-id="c4cad-194">22</span></span>

<span data-ttu-id="c4cad-195">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c4cad-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-196">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c4cad-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-197">23</span><span class="sxs-lookup"><span data-stu-id="c4cad-197">23</span></span>

<span data-ttu-id="c4cad-198">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c4cad-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-199">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="c4cad-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-200">24</span><span class="sxs-lookup"><span data-stu-id="c4cad-200">24</span></span>

<span data-ttu-id="c4cad-201">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="c4cad-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4cad-202">**Andere**</span><span class="sxs-lookup"><span data-stu-id="c4cad-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c4cad-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c4cad-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c4cad-204">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4cad-204">Examples</span></span>

<span data-ttu-id="c4cad-205">Im folgenden wird der Start Modus eines Dienstanbieter geändert, wenn der Start [Modus eines Dienst](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) -PowerShell-Beispiels aus der TechNet Gallery abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4cad-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="c4cad-206">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4cad-206">Requirements</span></span>



| <span data-ttu-id="c4cad-207">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4cad-207">Requirement</span></span> | <span data-ttu-id="c4cad-208">Wert</span><span class="sxs-lookup"><span data-stu-id="c4cad-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cad-209">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4cad-209">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cad-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4cad-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4cad-211">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4cad-211">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cad-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4cad-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4cad-213">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4cad-213">Namespace</span></span><br/>                | <span data-ttu-id="c4cad-214">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c4cad-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c4cad-215">MOF</span><span class="sxs-lookup"><span data-stu-id="c4cad-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4cad-216"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4cad-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4cad-217">DLL</span><span class="sxs-lookup"><span data-stu-id="c4cad-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4cad-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4cad-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4cad-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4cad-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4cad-220">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4cad-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c4cad-221">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c4cad-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c4cad-222">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="c4cad-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

