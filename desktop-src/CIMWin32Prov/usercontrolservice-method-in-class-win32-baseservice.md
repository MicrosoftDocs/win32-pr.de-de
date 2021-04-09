---
description: Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: UserControlService-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861599"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="27c18-103">UserControlService-Methode der Win32 \_ baseservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="27c18-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="27c18-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="27c18-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="27c18-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="27c18-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="27c18-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="27c18-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="27c18-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="27c18-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="27c18-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27c18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c18-109">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27c18-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c18-110">Ein-Wert, der einen Steuerungs Befehl für einen Dienst angibt.</span><span class="sxs-lookup"><span data-stu-id="27c18-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="27c18-111">Ein Steuerelement Befehl ist beispielsweise ein Befehl zum Anhalten oder fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="27c18-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="27c18-112">Der Wert kann ein vordefinierter Code oder ein Wert und eine Aktion sein, die der Dienst definiert.</span><span class="sxs-lookup"><span data-stu-id="27c18-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="27c18-113">Im folgenden sind die vordefinierten Kontrollcodes aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="27c18-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="27c18-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**Dienst \_ Steuerung \_ fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="27c18-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-115">Benachrichtigt einen angehaltenen Dienst, fortgesetzt zu werden.</span><span class="sxs-lookup"><span data-stu-id="27c18-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="27c18-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**Dienst \_ Steuerungs \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="27c18-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-117">Benachrichtigt einen Dienst, die aktuellen Statusinformationen an den Dienststeuerungs-Manager zu melden.</span><span class="sxs-lookup"><span data-stu-id="27c18-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="27c18-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**Dienst \_ Steuerung \_ netbindadd**</span><span class="sxs-lookup"><span data-stu-id="27c18-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-119">Benachrichtigt einen Netzwerkdienst, dass eine neue Komponente für die Bindung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="27c18-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="27c18-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**Dienst \_ Steuerung \_ netbinddeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="27c18-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-121">Benachrichtigt einen Netzwerkdienst, dass eine seiner Bindungen deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27c18-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="27c18-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**Dienst \_ Steuerung \_ netbindenable**</span><span class="sxs-lookup"><span data-stu-id="27c18-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-123">Benachrichtigt einen Netzwerkdienst, dass eine deaktivierte Bindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27c18-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="27c18-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**Dienst \_ Steuerung \_ netbindremove**</span><span class="sxs-lookup"><span data-stu-id="27c18-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-125">Benachrichtigt einen Netzwerkdienst, dass eine Komponente für die Bindung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="27c18-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="27c18-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**Dienststeuerungs- \_ \_ paramchange**</span><span class="sxs-lookup"><span data-stu-id="27c18-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-127">Benachrichtigt einen Dienst, dass seine Startparameter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="27c18-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="27c18-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**Dienst \_ Steuerungs \_ Pause**</span><span class="sxs-lookup"><span data-stu-id="27c18-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-129">Benachrichtigt einen Dienst, anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="27c18-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="27c18-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**Dienst \_ Steuerungs \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="27c18-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="27c18-131">Benachrichtigt einen Dienst, anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="27c18-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c18-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27c18-132">Return value</span></span>

<span data-ttu-id="27c18-133">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="27c18-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="27c18-134">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="27c18-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-135">0</span><span class="sxs-lookup"><span data-stu-id="27c18-135">0</span></span>

<span data-ttu-id="27c18-136">Die Anforderung wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="27c18-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-137">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="27c18-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-138">1</span><span class="sxs-lookup"><span data-stu-id="27c18-138">1</span></span>

<span data-ttu-id="27c18-139">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27c18-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-140">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="27c18-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-141">2</span><span class="sxs-lookup"><span data-stu-id="27c18-141">2</span></span>

<span data-ttu-id="27c18-142">Der Benutzer verfügt nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="27c18-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-143">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="27c18-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-144">3</span><span class="sxs-lookup"><span data-stu-id="27c18-144">3</span></span>

<span data-ttu-id="27c18-145">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="27c18-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-146">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="27c18-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-147">4</span><span class="sxs-lookup"><span data-stu-id="27c18-147">4</span></span>

<span data-ttu-id="27c18-148">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="27c18-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-149">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="27c18-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-150">5</span><span class="sxs-lookup"><span data-stu-id="27c18-150">5</span></span>

<span data-ttu-id="27c18-151">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="27c18-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-152">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="27c18-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-153">6</span><span class="sxs-lookup"><span data-stu-id="27c18-153">6</span></span>

<span data-ttu-id="27c18-154">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="27c18-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-155">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="27c18-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-156">7</span><span class="sxs-lookup"><span data-stu-id="27c18-156">7</span></span>

<span data-ttu-id="27c18-157">Der Dienst antwortet nicht schnell auf die Start Anforderung.</span><span class="sxs-lookup"><span data-stu-id="27c18-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-158">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="27c18-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-159">8</span><span class="sxs-lookup"><span data-stu-id="27c18-159">8</span></span>

<span data-ttu-id="27c18-160">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="27c18-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-161">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="27c18-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-162">9</span><span class="sxs-lookup"><span data-stu-id="27c18-162">9</span></span>

<span data-ttu-id="27c18-163">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="27c18-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-164">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="27c18-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-165">10</span><span class="sxs-lookup"><span data-stu-id="27c18-165">10</span></span>

<span data-ttu-id="27c18-166">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27c18-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-167">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="27c18-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-168">11</span><span class="sxs-lookup"><span data-stu-id="27c18-168">11</span></span>

<span data-ttu-id="27c18-169">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="27c18-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-170">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="27c18-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-171">12</span><span class="sxs-lookup"><span data-stu-id="27c18-171">12</span></span>

<span data-ttu-id="27c18-172">Eine Abhängigkeit, von der dieser Dienst abhängt, wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="27c18-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-173">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="27c18-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-174">13</span><span class="sxs-lookup"><span data-stu-id="27c18-174">13</span></span>

<span data-ttu-id="27c18-175">Der Dienst findet den von einem abhängigen Dienst benötigten Dienst nicht.</span><span class="sxs-lookup"><span data-stu-id="27c18-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-176">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="27c18-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-177">14</span><span class="sxs-lookup"><span data-stu-id="27c18-177">14</span></span>

<span data-ttu-id="27c18-178">Der Dienst ist im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="27c18-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-179">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="27c18-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-180">15</span><span class="sxs-lookup"><span data-stu-id="27c18-180">15</span></span>

<span data-ttu-id="27c18-181">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="27c18-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-182">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="27c18-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-183">16</span><span class="sxs-lookup"><span data-stu-id="27c18-183">16</span></span>

<span data-ttu-id="27c18-184">Der Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="27c18-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-185">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="27c18-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-186">17</span><span class="sxs-lookup"><span data-stu-id="27c18-186">17</span></span>

<span data-ttu-id="27c18-187">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="27c18-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-188">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="27c18-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-189">18</span><span class="sxs-lookup"><span data-stu-id="27c18-189">18</span></span>

<span data-ttu-id="27c18-190">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="27c18-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-191">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="27c18-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-192">19</span><span class="sxs-lookup"><span data-stu-id="27c18-192">19</span></span>

<span data-ttu-id="27c18-193">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27c18-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-194">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="27c18-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-195">20</span><span class="sxs-lookup"><span data-stu-id="27c18-195">20</span></span>

<span data-ttu-id="27c18-196">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="27c18-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-197">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="27c18-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-198">21</span><span class="sxs-lookup"><span data-stu-id="27c18-198">21</span></span>

<span data-ttu-id="27c18-199">Ungültige Parameter wurden an den Dienst übermittelt.</span><span class="sxs-lookup"><span data-stu-id="27c18-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-200">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="27c18-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-201">22</span><span class="sxs-lookup"><span data-stu-id="27c18-201">22</span></span>

<span data-ttu-id="27c18-202">Das Konto, unter dem dieser Dienst ausgeführt wird, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="27c18-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-203">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="27c18-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-204">23</span><span class="sxs-lookup"><span data-stu-id="27c18-204">23</span></span>

<span data-ttu-id="27c18-205">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="27c18-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-206">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="27c18-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-207">24</span><span class="sxs-lookup"><span data-stu-id="27c18-207">24</span></span>

<span data-ttu-id="27c18-208">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="27c18-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="27c18-209">**Andere**</span><span class="sxs-lookup"><span data-stu-id="27c18-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="27c18-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="27c18-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27c18-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27c18-211">Requirements</span></span>



| <span data-ttu-id="27c18-212">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27c18-212">Requirement</span></span> | <span data-ttu-id="27c18-213">Wert</span><span class="sxs-lookup"><span data-stu-id="27c18-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27c18-214">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27c18-214">Minimum supported client</span></span><br/> | <span data-ttu-id="27c18-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27c18-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27c18-216">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27c18-216">Minimum supported server</span></span><br/> | <span data-ttu-id="27c18-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27c18-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27c18-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="27c18-218">Namespace</span></span><br/>                | <span data-ttu-id="27c18-219">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="27c18-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27c18-220">MOF</span><span class="sxs-lookup"><span data-stu-id="27c18-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27c18-221"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="27c18-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27c18-222">DLL</span><span class="sxs-lookup"><span data-stu-id="27c18-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27c18-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27c18-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c18-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27c18-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="27c18-225">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27c18-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="27c18-226">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="27c18-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

