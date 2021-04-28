---
title: Create-Methode der Win32_Service -Klasse (Remotedesktopdienste)
description: 'Create-Methode der Win32_Service -Klasse (Remotedesktopdienste): Erstellt einen neuen Systemdienst.'
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Erstellen einer Remotedesktopdienste
- Create method Remotedesktopdienste , Win32_Service class
- Win32_Service klasse Remotedesktopdienste , Create-Methode
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9daf877f56bb7e9bfcc349e4efb38635a9286a48
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090688"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="221b4-106">Create-Methode der Win32_Service -Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="221b4-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="221b4-107">Die **Create** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) erstellt einen neuen Systemdienst.</span><span class="sxs-lookup"><span data-stu-id="221b4-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="221b4-108">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="221b4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="221b4-109">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="221b4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="221b4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="221b4-110">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="221b4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="221b4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="221b4-112">*Name* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-113">Name des Diensts, der in der **Create-Methode installiert werden** soll.</span><span class="sxs-lookup"><span data-stu-id="221b4-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="221b4-114">Die maximale Zeichenfolgenlänge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="221b4-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="221b4-115">Die Service Control Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen bei, bei Dienstnamenvergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="221b4-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="221b4-116">Schrägstriche (/) und doppelte schräge Schrägstriche ( \) sind ungültige Dienstnamenzeichen.</span><span class="sxs-lookup"><span data-stu-id="221b4-116">Forward-slashes (/) and double back-slashes (\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-117">*DisplayName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-118">Anzeigename des Diensts.</span><span class="sxs-lookup"><span data-stu-id="221b4-118">Display name of the service.</span></span> <span data-ttu-id="221b4-119">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="221b4-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="221b4-120">Der Name wird im Dienststeuerungs-Manager beibehalten.</span><span class="sxs-lookup"><span data-stu-id="221b4-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="221b4-121">*Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="221b4-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="221b4-122">Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*</span><span class="sxs-lookup"><span data-stu-id="221b4-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="221b4-123">Beispiel: "Atdisk".</span><span class="sxs-lookup"><span data-stu-id="221b4-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="221b4-124">*PathName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-125">Vollqualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="221b4-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="221b4-126">Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="221b4-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="221b4-127">*ServiceType* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-128">Typ der Dienste, die für Prozesse bereitgestellt werden, die sie aufrufen.</span><span class="sxs-lookup"><span data-stu-id="221b4-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="221b4-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="221b4-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-130">Kerneltreiber</span><span class="sxs-lookup"><span data-stu-id="221b4-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="221b4-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="221b4-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-132">Dateisystemtreiber</span><span class="sxs-lookup"><span data-stu-id="221b4-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="221b4-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="221b4-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-134">Adapter</span><span class="sxs-lookup"><span data-stu-id="221b4-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="221b4-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="221b4-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-136">Recognizer Driver</span><span class="sxs-lookup"><span data-stu-id="221b4-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="221b4-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="221b4-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-138">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="221b4-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="221b4-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="221b4-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-140">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="221b4-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="221b4-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="221b4-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="221b4-142">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="221b4-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="221b4-143">*ErrorControl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-144">Schweregrad des Fehlers, wenn die **Create-Methode** nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="221b4-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="221b4-145">Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="221b4-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="221b4-146">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="221b4-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="221b4-147">0</span><span class="sxs-lookup"><span data-stu-id="221b4-147">0</span></span>
</dt> <dd>

<span data-ttu-id="221b4-148">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="221b4-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-149">1</span><span class="sxs-lookup"><span data-stu-id="221b4-149">1</span></span>
</dt> <dd>

<span data-ttu-id="221b4-150">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="221b4-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-151">2</span><span class="sxs-lookup"><span data-stu-id="221b4-151">2</span></span>
</dt> <dd>

<span data-ttu-id="221b4-152">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="221b4-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-153">3</span><span class="sxs-lookup"><span data-stu-id="221b4-153">3</span></span>
</dt> <dd>

<span data-ttu-id="221b4-154">Das System versucht, mit einer guten Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="221b4-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="221b4-155">*StartMode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-156">Startmodus des Windows-Basisdiensts.</span><span class="sxs-lookup"><span data-stu-id="221b4-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="221b4-157">Start</span><span class="sxs-lookup"><span data-stu-id="221b4-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="221b4-158">Vom Betriebssystemladeprogramm gestarteter Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="221b4-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="221b4-159">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="221b4-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-160">System</span><span class="sxs-lookup"><span data-stu-id="221b4-160">System</span></span>
</dt> <dd>

<span data-ttu-id="221b4-161">Der Vom Initialisierungsprozess des Betriebssystems gestartete Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="221b4-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="221b4-162">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="221b4-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-163">Automatische</span><span class="sxs-lookup"><span data-stu-id="221b4-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="221b4-164">Der Dienst wird während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet.</span><span class="sxs-lookup"><span data-stu-id="221b4-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-165">Manuell</span><span class="sxs-lookup"><span data-stu-id="221b4-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="221b4-166">Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](win32-terminalservice-startservice.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="221b4-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-167">Disabled</span><span class="sxs-lookup"><span data-stu-id="221b4-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="221b4-168">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="221b4-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="221b4-169">*DesktopInteract* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-170">True gibt an, dass der Dienst Windows auf dem Desktop erstellen oder mit ihnen kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="221b4-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-171">*StartName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-172">Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="221b4-172">Account name under which the service runs.</span></span> <span data-ttu-id="221b4-173">Je nach Diensttyp kann der Kontoname im Format DomainName \\ Username oder User Principal Name (UPN) () Username@DomainName vorliegen.</span><span class="sxs-lookup"><span data-stu-id="221b4-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="221b4-174">Der Dienstprozess wird bei der Ausführung in einer dieser beiden Formen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="221b4-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="221b4-175">Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="221b4-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="221b4-176">Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="221b4-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="221b4-177">Für Treiber auf Kernel- oder Systemebene enthält *StartName* den Namen des Treiberobjekts (d.h. \\ FileSystem \\ Rdr oder \\ Driver \\ Xns), den das E/A-System zum Laden des Gerätetreibers verwendet.</span><span class="sxs-lookup"><span data-stu-id="221b4-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="221b4-178">Wenn **NULL** angegeben ist, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="221b4-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="221b4-179">Beispiel: DWDOM \\ Admin.</span><span class="sxs-lookup"><span data-stu-id="221b4-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-180">*StartPassword* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-181">Kennwort für den vom *StartName-Parameter* angegebenen Kontonamen.</span><span class="sxs-lookup"><span data-stu-id="221b4-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="221b4-182">Geben Sie **NULL** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="221b4-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="221b4-183">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="221b4-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-184">*LoadOrderGroup* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-185">Gruppenname, der dem neuen Dienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="221b4-185">Group name associated with the new service.</span></span> <span data-ttu-id="221b4-186">Ladereihenfolgengruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="221b4-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="221b4-187">Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="221b4-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="221b4-188">Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter* aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="221b4-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="221b4-189">Dienste in der Liste der Ladereihenfolgegruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Lastenreihenfolgegruppen enthalten sind, gefolgt von Diensten, die keiner Gruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="221b4-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="221b4-190">Die Registrierung verfügt über eine Liste der Ladereihenfolgegruppen unter:</span><span class="sxs-lookup"><span data-stu-id="221b4-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="221b4-191">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="221b4-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="221b4-192">*LoadOrderGroupDependencies* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-193">Array von Lastreihenfolgegruppen, die vor diesem Dienst gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="221b4-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="221b4-194">Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet.</span><span class="sxs-lookup"><span data-stu-id="221b4-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="221b4-195">In Visual Basic oder Skripts können Sie ein vbArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="221b4-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="221b4-196">Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="221b4-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="221b4-197">Gruppennamen muss das **Zeichen SC GROUP \_ \_ IDENTIFIER** (definiert in der Datei Winsvc.h) vorangestellt sein, um sie von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="221b4-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="221b4-198">Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="221b4-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-199">*ServiceDependencies* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="221b4-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="221b4-200">Array, das Namen von Diensten enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="221b4-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="221b4-201">Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet.</span><span class="sxs-lookup"><span data-stu-id="221b4-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="221b4-202">In Visual Basic oder Skripts können Sie ein vbArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="221b4-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="221b4-203">Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="221b4-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="221b4-204">Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="221b4-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="221b4-205">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="221b4-205">Return value</span></span>

<span data-ttu-id="221b4-206">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="221b4-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="221b4-207">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="221b4-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="221b4-208">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="221b4-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="221b4-209">**0**</span><span class="sxs-lookup"><span data-stu-id="221b4-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-210">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="221b4-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-211">**1**</span><span class="sxs-lookup"><span data-stu-id="221b4-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-212">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="221b4-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-213">**2**</span><span class="sxs-lookup"><span data-stu-id="221b4-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-214">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="221b4-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-215">**3**</span><span class="sxs-lookup"><span data-stu-id="221b4-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-216">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="221b4-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-217">**4**</span><span class="sxs-lookup"><span data-stu-id="221b4-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-218">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="221b4-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-219">**5**</span><span class="sxs-lookup"><span data-stu-id="221b4-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-220">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts **(State-Eigenschaft** der [**Win32 \_ BaseService-Klasse)**](/windows/desktop/CIMWin32Prov/win32-baseservice) gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="221b4-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-221">**6**</span><span class="sxs-lookup"><span data-stu-id="221b4-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-222">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="221b4-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-223">**7**</span><span class="sxs-lookup"><span data-stu-id="221b4-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-224">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="221b4-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-225">**8**</span><span class="sxs-lookup"><span data-stu-id="221b4-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-226">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="221b4-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-227">**9**</span><span class="sxs-lookup"><span data-stu-id="221b4-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-228">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="221b4-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-229">**10**</span><span class="sxs-lookup"><span data-stu-id="221b4-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-230">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="221b4-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-231">**11**</span><span class="sxs-lookup"><span data-stu-id="221b4-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-232">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="221b4-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-233">**12**</span><span class="sxs-lookup"><span data-stu-id="221b4-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-234">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="221b4-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-235">**13**</span><span class="sxs-lookup"><span data-stu-id="221b4-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-236">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="221b4-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-237">**14**</span><span class="sxs-lookup"><span data-stu-id="221b4-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-238">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="221b4-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-239">**15**</span><span class="sxs-lookup"><span data-stu-id="221b4-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-240">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="221b4-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-241">**16**</span><span class="sxs-lookup"><span data-stu-id="221b4-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-242">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="221b4-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-243">**17**</span><span class="sxs-lookup"><span data-stu-id="221b4-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-244">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="221b4-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-245">**18**</span><span class="sxs-lookup"><span data-stu-id="221b4-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-246">Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="221b4-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-247">**19**</span><span class="sxs-lookup"><span data-stu-id="221b4-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-248">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="221b4-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-249">**20**</span><span class="sxs-lookup"><span data-stu-id="221b4-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-250">Der Dienstname weist ungültige Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="221b4-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-251">**21**</span><span class="sxs-lookup"><span data-stu-id="221b4-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-252">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="221b4-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-253">**22**</span><span class="sxs-lookup"><span data-stu-id="221b4-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-254">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="221b4-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-255">**23**</span><span class="sxs-lookup"><span data-stu-id="221b4-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-256">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="221b4-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="221b4-257">**24**</span><span class="sxs-lookup"><span data-stu-id="221b4-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="221b4-258">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="221b4-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="221b4-259">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="221b4-259">Remarks</span></span>

<span data-ttu-id="221b4-260">Dienste werden im Allgemeinen auf zwei Arten installiert: entweder als Teil der Betriebssysteminstallation oder mithilfe eines vom Dienstentwickler bereitgestellten Installationsprogramms.</span><span class="sxs-lookup"><span data-stu-id="221b4-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="221b4-261">Einige Dienste, insbesondere solche, die im Unternehmen erstellt wurden, verfügen jedoch möglicherweise nicht über ein Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="221b4-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="221b4-262">In diesen Fällen können Sie die **Create-Methode** verwenden, um Dienste programmgesteuert zu installieren.</span><span class="sxs-lookup"><span data-stu-id="221b4-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="221b4-263">Trotz des Namens erstellt die Create-Methode keinen Dienst. Es wird lediglich ein vorhandener Dienst installiert.</span><span class="sxs-lookup"><span data-stu-id="221b4-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="221b4-264">Um diesen Befehl verwenden zu können, müssen Sie die ausführbare Datei des Diensts auf einen Computer kopieren und dann **erstellen** verwenden, um den Dienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="221b4-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="221b4-265">Die **Create-Methode** ähnelt der [**Change-Methode.**](win32-terminalservice-change.md)</span><span class="sxs-lookup"><span data-stu-id="221b4-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="221b4-266">In beiden Fällen werden die Eigenschaften des Diensts als Parameter an die -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="221b4-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="221b4-267">Wie bei den Parametern, die mit der **Change-Methode** verwendet werden, ist die Reihenfolge, in der diese Parameter übergeben werden, sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="221b4-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="221b4-268">Der *LoadOrderGroup-Parameter* stellt eine Gruppierung von Systemdiensten dar, die Ausführungsabhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="221b4-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="221b4-269">Die Dienste müssen in der von der Lastauftragsgruppe angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="221b4-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="221b4-270">Diese abhängigen Dienste erfordern das Vorhandensein der voraussenten Dienste, damit sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="221b4-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="221b4-271">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="221b4-271">Requirements</span></span>



| <span data-ttu-id="221b4-272">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="221b4-272">Requirement</span></span> | <span data-ttu-id="221b4-273">Wert</span><span class="sxs-lookup"><span data-stu-id="221b4-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="221b4-274">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="221b4-274">Minimum supported client</span></span><br/> | <span data-ttu-id="221b4-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="221b4-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="221b4-276">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="221b4-276">Minimum supported server</span></span><br/> | <span data-ttu-id="221b4-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="221b4-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="221b4-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="221b4-278">Namespace</span></span><br/>                | <span data-ttu-id="221b4-279">\\ \\ CiMv2-Stammterminaldienste</span><span class="sxs-lookup"><span data-stu-id="221b4-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="221b4-280">MOF</span><span class="sxs-lookup"><span data-stu-id="221b4-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="221b4-281"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="221b4-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="221b4-282">DLL</span><span class="sxs-lookup"><span data-stu-id="221b4-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="221b4-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="221b4-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="221b4-284">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="221b4-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221b4-285">**Win32-Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="221b4-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="221b4-286">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="221b4-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="221b4-287">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="221b4-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="221b4-288">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="221b4-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

