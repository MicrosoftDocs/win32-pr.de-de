---
description: 'Create method of the Win32_Service class (CIMWin32 WMI Providers) ( Create method of the Win32_Service Class (CIMWin32 WMI Providers)): Erstellt einen neuen Systemdienst.'
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Create-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71bc0f4edb879fc4a51a012bc53db67031056f47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089689"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="5f9d7-103">Create-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5f9d7-104">Die **Create** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) erstellt einen neuen Systemdienst.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="5f9d7-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5f9d7-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f9d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f9d7-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5f9d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f9d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f9d7-109">*Name* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-110">Name des Diensts, der in der **Create-Methode installiert werden** soll.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="5f9d7-111">Die maximale Zeichenfolgenlänge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="5f9d7-112">Die Service Control Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen bei, bei Dienstnamenvergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="5f9d7-113">Schrägstriche (/) und doppelte schräge Schrägstriche \\ () sind ungültige Dienstnamenzeichen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-114">*DisplayName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-115">Anzeigename des Diensts.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-115">Display name of the service.</span></span> <span data-ttu-id="5f9d7-116">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="5f9d7-117">Der Name wird im Dienststeuerungs-Manager beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="5f9d7-118">*Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="5f9d7-119">Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*</span><span class="sxs-lookup"><span data-stu-id="5f9d7-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="5f9d7-120">Beispiel: "Atdisk".</span><span class="sxs-lookup"><span data-stu-id="5f9d7-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-121">*PathName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-122">Vollqualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="5f9d7-123">Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="5f9d7-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-124">*ServiceType* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-125">Typ der Dienste, die für Prozesse bereitgestellt werden, die sie aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="5f9d7-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-127">Kerneltreiber</span><span class="sxs-lookup"><span data-stu-id="5f9d7-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-129">Dateisystemtreiber</span><span class="sxs-lookup"><span data-stu-id="5f9d7-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-131">Adapter</span><span class="sxs-lookup"><span data-stu-id="5f9d7-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-133">Erkennungstreiber</span><span class="sxs-lookup"><span data-stu-id="5f9d7-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-135">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="5f9d7-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-137">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="5f9d7-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-139">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="5f9d7-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5f9d7-140">*ErrorControl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-141">Schweregrad des Fehlers, wenn die **Create-Methode** nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="5f9d7-142">Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="5f9d7-143">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="5f9d7-144">0</span><span class="sxs-lookup"><span data-stu-id="5f9d7-144">0</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-145">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-146">1</span><span class="sxs-lookup"><span data-stu-id="5f9d7-146">1</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-147">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-148">2</span><span class="sxs-lookup"><span data-stu-id="5f9d7-148">2</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-149">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-150">3</span><span class="sxs-lookup"><span data-stu-id="5f9d7-150">3</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-151">Das System versucht, mit einer guten Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5f9d7-152">*StartMode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-153">Startmodus des Windows-Basisdiensts.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="5f9d7-154">Start</span><span class="sxs-lookup"><span data-stu-id="5f9d7-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-155">Vom Betriebssystemlader gestarteter Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="5f9d7-156">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-157">System</span><span class="sxs-lookup"><span data-stu-id="5f9d7-157">System</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-158">Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="5f9d7-159">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-160">Automatische</span><span class="sxs-lookup"><span data-stu-id="5f9d7-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-161">Der Dienst wird automatisch vom Dienststeuerungs-Manager während des Systemstarts gestartet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-162">Manuell</span><span class="sxs-lookup"><span data-stu-id="5f9d7-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-163">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-service.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="5f9d7-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-165">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5f9d7-166">*DesktopInteract* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-167">True **gibt an,** dass der Dienst Fenster auf dem Desktop erstellen oder mit ihnen kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-168">*StartName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-169">Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-169">Account name under which the service runs.</span></span> <span data-ttu-id="5f9d7-170">Je nach Diensttyp kann der Kontoname das Format DomainName Username oder \\ UpN (UpN) (Benutzerprinzipalname ( ) Username@DomainName haben.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="5f9d7-171">Der Dienstprozess wird mit einer dieser beiden Formen protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="5f9d7-172">Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="5f9d7-173">Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="5f9d7-174">Für Einen Kernel oder Treiber auf Systemebene enthält *StartName* den Namen des Treiberobjekts (d. h. FileSystem Rdr oder Driver Xns), den das Eingabe- und Ausgabesystem \\ \\ \\ (E/A) zum Laden des \\ Gerätetreibers verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="5f9d7-175">Wenn **NULL** angegeben ist, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="5f9d7-176">Beispiel: \\ DWDOM-Administrator.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-177">*StartPassword* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-178">Kennwort für den Kontonamen, der durch den *StartName-Parameter angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="5f9d7-179">Geben **Sie NULL** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="5f9d7-180">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-181">*LoadOrderGroup* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-182">Gruppenname, der dem neuen Dienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-182">Group name associated with the new service.</span></span> <span data-ttu-id="5f9d7-183">Ladereihenfolgengruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="5f9d7-184">Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="5f9d7-185">Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter* aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="5f9d7-186">Dienste in der Liste der Ladereihenfolgegruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Lastenreihenfolgegruppen enthalten sind, gefolgt von Diensten, die keiner Gruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="5f9d7-187">Die Registrierung verfügt über eine Liste der Ladereihenfolgegruppen unter:</span><span class="sxs-lookup"><span data-stu-id="5f9d7-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="5f9d7-188">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-189">*LoadOrderGroupDependencies* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-190">Array von Lastreihenfolgegruppen, die vor diesem Dienst gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="5f9d7-191">Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="5f9d7-192">In Visual Basic oder Skripts können Sie ein vbArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="5f9d7-193">Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5f9d7-194">Gruppennamen muss das **Zeichen SC GROUP \_ \_ IDENTIFIER** (definiert in der Datei Winsvc.h) vorangestellt sein, um sie von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="5f9d7-195">Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-196">*ServiceDependencies* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5f9d7-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-197">Array, das Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="5f9d7-198">Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="5f9d7-199">In Visual Basic oder Skripts können Sie ein vbArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="5f9d7-200">Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5f9d7-201">Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst ausgeführt wird, von dem er abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f9d7-202">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f9d7-202">Return value</span></span>

<span data-ttu-id="5f9d7-203">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um auf einen Fehler hindeuten zu können.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="5f9d7-204">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5f9d7-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5f9d7-205">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5f9d7-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5f9d7-206">**0**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-207">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-208">**1**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-209">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-210">**2**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-211">Der Benutzer hatte nicht den erforderlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-212">**3**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-213">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-214">**4**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-215">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-216">**5**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-217">Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts **(State-Eigenschaft** der [**Win32 \_ BaseService-Klasse)**](win32-baseservice.md) gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-218">**6**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-219">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-220">**7**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-221">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-222">**8**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-223">Unbekannter Fehler beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-224">**9**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-225">Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-226">**10**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-227">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-228">**11**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-229">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-230">**12**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-231">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-232">**13**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-233">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-234">**14**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-235">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-236">**15**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-237">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-238">**16**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-239">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-240">**17**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-241">Der Dienst verfügt über keinen Ausführungsthread.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-242">**18**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-243">Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-244">**19**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-245">Ein Dienst wird unter demselben Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-246">**20**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-247">Der Dienstname enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-248">**21**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-249">Ungültige Parameter wurden an den Dienst übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-250">**22**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-251">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-252">**23**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-253">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d7-254">**24**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5f9d7-255">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f9d7-256">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f9d7-256">Remarks</span></span>

<span data-ttu-id="5f9d7-257">Dienste werden im Allgemeinen auf zwei Arten installiert: entweder als Teil der Betriebssysteminstallation oder mithilfe eines vom Dienstentwickler bereitgestellten Installationsprogramms.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="5f9d7-258">Einige Dienste, insbesondere solche, die im Unternehmen erstellt wurden, verfügen jedoch möglicherweise nicht über ein Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="5f9d7-259">In diesen Fällen können Sie die **Create-Methode** verwenden, um Dienste programmgesteuert zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="5f9d7-260">Trotz des Namens erstellt die Create-Methode keinen Dienst. Es wird lediglich ein vorhandener Dienst installiert.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="5f9d7-261">Um diesen Befehl zu verwenden, müssen Sie die ausführbare Datei des Diensts auf einen Computer kopieren und dann **Erstellen** verwenden, um den Dienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="5f9d7-262">Die **Create-Methode** ähnelt der [**Change-Methode.**](change-method-in-class-win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="5f9d7-263">In beiden Fällen werden die Eigenschaften des Diensts als Parameter an die -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="5f9d7-264">Wie bei den Parametern, die mit der **Change-Methode** verwendet werden, ist die Reihenfolge, in der diese Parameter übergeben werden, sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="5f9d7-265">Der *LoadOrderGroup-Parameter* stellt eine Gruppierung von Systemdiensten dar, die Ausführungsabhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="5f9d7-266">Die Dienste müssen in der von der Load Order Group angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="5f9d7-267">Diese abhängigen Dienste erfordern, dass die Vorgängerdienste vorhanden sind, damit sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="5f9d7-268">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f9d7-268">Examples</span></span>

<span data-ttu-id="5f9d7-269">Der folgende VBScript-Code installiert einen Dienst mit dem Namen DbService.</span><span class="sxs-lookup"><span data-stu-id="5f9d7-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="5f9d7-270">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f9d7-270">Requirements</span></span>



| <span data-ttu-id="5f9d7-271">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f9d7-271">Requirement</span></span> | <span data-ttu-id="5f9d7-272">Wert</span><span class="sxs-lookup"><span data-stu-id="5f9d7-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9d7-273">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-273">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9d7-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f9d7-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f9d7-275">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f9d7-275">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9d7-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f9d7-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f9d7-277">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f9d7-277">Namespace</span></span><br/>                | <span data-ttu-id="5f9d7-278">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5f9d7-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f9d7-279">MOF</span><span class="sxs-lookup"><span data-stu-id="5f9d7-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f9d7-280"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f9d7-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f9d7-281">DLL</span><span class="sxs-lookup"><span data-stu-id="5f9d7-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f9d7-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f9d7-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f9d7-283">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f9d7-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f9d7-284">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f9d7-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5f9d7-285">**\_Win32-Dienst**</span><span class="sxs-lookup"><span data-stu-id="5f9d7-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="5f9d7-286">WMI-Aufgaben: Dienste</span><span class="sxs-lookup"><span data-stu-id="5f9d7-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

