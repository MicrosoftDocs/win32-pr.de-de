---
description: Ändert den Start Modus eines Dienst Objekts, das von Win32 \_ baseservice abgeleitet ist.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: ChangeStartMode-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126686"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="1aaae-103">ChangeStartMode-Methode der Win32 \_ baseservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1aaae-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="1aaae-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **ChangeStartMode** ändert den Start Modus eines Dienst Objekts, das von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="1aaae-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="1aaae-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1aaae-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1aaae-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1aaae-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1aaae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aaae-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="1aaae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aaae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aaae-109">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1aaae-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-110">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="1aaae-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="1aaae-111">Der Standardwert ist "automatisch".</span><span class="sxs-lookup"><span data-stu-id="1aaae-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="1aaae-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="1aaae-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="1aaae-113">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="1aaae-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="1aaae-114">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="1aaae-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="1aaae-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span><span class="sxs-lookup"><span data-stu-id="1aaae-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="1aaae-116">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="1aaae-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="1aaae-117">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="1aaae-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="1aaae-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="1aaae-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="1aaae-119">Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1aaae-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="1aaae-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="1aaae-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="1aaae-121">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-baseservice.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="1aaae-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1aaae-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="1aaae-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="1aaae-123">Der Dienst ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1aaae-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aaae-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aaae-124">Return value</span></span>

<span data-ttu-id="1aaae-125">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1aaae-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1aaae-126">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="1aaae-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-127">0</span><span class="sxs-lookup"><span data-stu-id="1aaae-127">0</span></span>

<span data-ttu-id="1aaae-128">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1aaae-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-129">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="1aaae-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-130">1</span><span class="sxs-lookup"><span data-stu-id="1aaae-130">1</span></span>

<span data-ttu-id="1aaae-131">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-132">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="1aaae-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-133">2</span><span class="sxs-lookup"><span data-stu-id="1aaae-133">2</span></span>

<span data-ttu-id="1aaae-134">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="1aaae-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-135">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="1aaae-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-136">3</span><span class="sxs-lookup"><span data-stu-id="1aaae-136">3</span></span>

<span data-ttu-id="1aaae-137">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="1aaae-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-138">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-139">4</span><span class="sxs-lookup"><span data-stu-id="1aaae-139">4</span></span>

<span data-ttu-id="1aaae-140">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="1aaae-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-141">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-142">5</span><span class="sxs-lookup"><span data-stu-id="1aaae-142">5</span></span>

<span data-ttu-id="1aaae-143">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32 \_ baseservice**](win32-baseservice.md)[**State**](win32-baseservice.md) -Eigenschaft) gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="1aaae-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-144">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="1aaae-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-145">6</span><span class="sxs-lookup"><span data-stu-id="1aaae-145">6</span></span>

<span data-ttu-id="1aaae-146">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="1aaae-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-147">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="1aaae-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-148">7</span><span class="sxs-lookup"><span data-stu-id="1aaae-148">7</span></span>

<span data-ttu-id="1aaae-149">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="1aaae-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-150">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-151">8</span><span class="sxs-lookup"><span data-stu-id="1aaae-151">8</span></span>

<span data-ttu-id="1aaae-152">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="1aaae-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-153">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="1aaae-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-154">9</span><span class="sxs-lookup"><span data-stu-id="1aaae-154">9</span></span>

<span data-ttu-id="1aaae-155">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1aaae-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-156">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-157">10</span><span class="sxs-lookup"><span data-stu-id="1aaae-157">10</span></span>

<span data-ttu-id="1aaae-158">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-159">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="1aaae-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-160">11</span><span class="sxs-lookup"><span data-stu-id="1aaae-160">11</span></span>

<span data-ttu-id="1aaae-161">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-162">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="1aaae-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-163">12</span><span class="sxs-lookup"><span data-stu-id="1aaae-163">12</span></span>

<span data-ttu-id="1aaae-164">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-165">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="1aaae-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-166">13</span><span class="sxs-lookup"><span data-stu-id="1aaae-166">13</span></span>

<span data-ttu-id="1aaae-167">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1aaae-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-168">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="1aaae-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-169">14</span><span class="sxs-lookup"><span data-stu-id="1aaae-169">14</span></span>

<span data-ttu-id="1aaae-170">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1aaae-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-171">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="1aaae-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-172">15</span><span class="sxs-lookup"><span data-stu-id="1aaae-172">15</span></span>

<span data-ttu-id="1aaae-173">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1aaae-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-174">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-175">16</span><span class="sxs-lookup"><span data-stu-id="1aaae-175">16</span></span>

<span data-ttu-id="1aaae-176">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-177">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="1aaae-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-178">17</span><span class="sxs-lookup"><span data-stu-id="1aaae-178">17</span></span>

<span data-ttu-id="1aaae-179">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="1aaae-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-180">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="1aaae-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-181">18</span><span class="sxs-lookup"><span data-stu-id="1aaae-181">18</span></span>

<span data-ttu-id="1aaae-182">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1aaae-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-183">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="1aaae-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-184">19</span><span class="sxs-lookup"><span data-stu-id="1aaae-184">19</span></span>

<span data-ttu-id="1aaae-185">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-186">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="1aaae-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-187">20</span><span class="sxs-lookup"><span data-stu-id="1aaae-187">20</span></span>

<span data-ttu-id="1aaae-188">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1aaae-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-189">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-190">21</span><span class="sxs-lookup"><span data-stu-id="1aaae-190">21</span></span>

<span data-ttu-id="1aaae-191">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1aaae-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-192">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-193">22</span><span class="sxs-lookup"><span data-stu-id="1aaae-193">22</span></span>

<span data-ttu-id="1aaae-194">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="1aaae-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-195">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="1aaae-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-196">23</span><span class="sxs-lookup"><span data-stu-id="1aaae-196">23</span></span>

<span data-ttu-id="1aaae-197">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1aaae-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-198">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="1aaae-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-199">24</span><span class="sxs-lookup"><span data-stu-id="1aaae-199">24</span></span>

<span data-ttu-id="1aaae-200">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="1aaae-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaae-201">**Andere**</span><span class="sxs-lookup"><span data-stu-id="1aaae-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1aaae-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="1aaae-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1aaae-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aaae-203">Requirements</span></span>



| <span data-ttu-id="1aaae-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aaae-204">Requirement</span></span> | <span data-ttu-id="1aaae-205">Wert</span><span class="sxs-lookup"><span data-stu-id="1aaae-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aaae-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1aaae-206">Minimum supported client</span></span><br/> | <span data-ttu-id="1aaae-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1aaae-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1aaae-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1aaae-208">Minimum supported server</span></span><br/> | <span data-ttu-id="1aaae-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aaae-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1aaae-210">Namespace</span><span class="sxs-lookup"><span data-stu-id="1aaae-210">Namespace</span></span><br/>                | <span data-ttu-id="1aaae-211">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1aaae-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1aaae-212">MOF</span><span class="sxs-lookup"><span data-stu-id="1aaae-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aaae-213"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1aaae-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aaae-214">DLL</span><span class="sxs-lookup"><span data-stu-id="1aaae-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aaae-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aaae-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aaae-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aaae-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="1aaae-217">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1aaae-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1aaae-218">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="1aaae-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

