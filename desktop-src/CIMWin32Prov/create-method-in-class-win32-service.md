---
description: Erstellt einen neuen-Systemdienst.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Create-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
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
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749040"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="e9a41-103">Create-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="e9a41-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e9a41-104">Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen-Systemdienst.</span><span class="sxs-lookup"><span data-stu-id="e9a41-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="e9a41-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9a41-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e9a41-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a41-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e9a41-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9a41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a41-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-110">Name des Dienstanbieter, der in der **Create** -Methode installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9a41-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="e9a41-111">Die maximale Zeichen folgen Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="e9a41-112">Die Dienst Steuerungs Verwaltung behält die Groß-/Kleinschreibung der Zeichen bei. bei Dienstnamen vergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="e9a41-113">Vorwärts Schrägstriche (/) und doppelte umgekehrte Schrägstriche ( \\ ) sind ungültige Dienstnamen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-114">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-115">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e9a41-115">Display name of the service.</span></span> <span data-ttu-id="e9a41-116">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="e9a41-117">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e9a41-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="e9a41-118">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="e9a41-119">Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9a41-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="e9a41-120">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="e9a41-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-121">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-122">Voll qualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="e9a41-123">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="e9a41-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-124">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-125">Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="e9a41-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e9a41-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-127">Kernel Treiber</span><span class="sxs-lookup"><span data-stu-id="e9a41-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="e9a41-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-129">Datei System Treiber</span><span class="sxs-lookup"><span data-stu-id="e9a41-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e9a41-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-131">Adapter</span><span class="sxs-lookup"><span data-stu-id="e9a41-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="e9a41-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-133">Erkennungs Treiber</span><span class="sxs-lookup"><span data-stu-id="e9a41-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="e9a41-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-135">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="e9a41-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e9a41-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-137">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="e9a41-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="e9a41-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-139">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="e9a41-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e9a41-140">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-141">Der Schweregrad des Fehlers, wenn die **Create** -Methode nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9a41-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="e9a41-142">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="e9a41-143">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="e9a41-144">0</span><span class="sxs-lookup"><span data-stu-id="e9a41-144">0</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-145">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-146">1</span><span class="sxs-lookup"><span data-stu-id="e9a41-146">1</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-147">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-148">2</span><span class="sxs-lookup"><span data-stu-id="e9a41-148">2</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-149">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-150">3</span><span class="sxs-lookup"><span data-stu-id="e9a41-150">3</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-151">Das System versucht, mit einer guten Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e9a41-152">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-153">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e9a41-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="e9a41-154">Start</span><span class="sxs-lookup"><span data-stu-id="e9a41-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-155">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e9a41-156">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="e9a41-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-157">System</span><span class="sxs-lookup"><span data-stu-id="e9a41-157">System</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-158">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e9a41-159">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="e9a41-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-160">Automatisch</span><span class="sxs-lookup"><span data-stu-id="e9a41-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-161">Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-162">Manuell</span><span class="sxs-lookup"><span data-stu-id="e9a41-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-163">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="e9a41-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="e9a41-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-165">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9a41-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e9a41-166">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-167">**True** gibt an, dass der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="e9a41-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-168">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-169">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-169">Account name under which the service runs.</span></span> <span data-ttu-id="e9a41-170">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder "Benutzer Prinzipal Name (UPN) Format ()" aufweisen Username@DomainName .</span><span class="sxs-lookup"><span data-stu-id="e9a41-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="e9a41-171">Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="e9a41-172">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="e9a41-173">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="e9a41-174">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="e9a41-175">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9a41-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="e9a41-176">Beispiel: dwdom- \\ Administrator.</span><span class="sxs-lookup"><span data-stu-id="e9a41-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-177">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-178">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="e9a41-179">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e9a41-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="e9a41-180">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-181">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-182">Der dem neuen Dienst zugeordnete Gruppenname.</span><span class="sxs-lookup"><span data-stu-id="e9a41-182">Group name associated with the new service.</span></span> <span data-ttu-id="e9a41-183">Lade Auftrags Gruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="e9a41-184">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge verweist, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e9a41-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="e9a41-185">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="e9a41-186">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="e9a41-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="e9a41-187">Die Registrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="e9a41-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="e9a41-188">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="e9a41-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-189">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-190">Array von Gruppen für die Auslastungs Anordnung, die vor diesem Dienst gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="e9a41-191">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="e9a41-192">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="e9a41-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="e9a41-193">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="e9a41-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="e9a41-194">Gruppennamen muss der **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um ihn von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="e9a41-195">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="e9a41-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-196">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a41-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-197">Ein Array, das Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="e9a41-198">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="e9a41-199">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="e9a41-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="e9a41-200">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="e9a41-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="e9a41-201">Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a41-202">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9a41-202">Return value</span></span>

<span data-ttu-id="e9a41-203">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e9a41-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="e9a41-204">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e9a41-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e9a41-205">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e9a41-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e9a41-206">**0**</span><span class="sxs-lookup"><span data-stu-id="e9a41-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-207">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-208">**1**</span><span class="sxs-lookup"><span data-stu-id="e9a41-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-209">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-210">**2**</span><span class="sxs-lookup"><span data-stu-id="e9a41-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-211">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="e9a41-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-212">**3**</span><span class="sxs-lookup"><span data-stu-id="e9a41-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-213">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e9a41-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-214">**4**</span><span class="sxs-lookup"><span data-stu-id="e9a41-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-215">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="e9a41-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-216">**5**</span><span class="sxs-lookup"><span data-stu-id="e9a41-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-217">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts (**State** -Eigenschaft der [**Win32- \_ baseservice**](win32-baseservice.md) -Klasse) gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="e9a41-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-218">**6**</span><span class="sxs-lookup"><span data-stu-id="e9a41-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-219">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-220">**7**</span><span class="sxs-lookup"><span data-stu-id="e9a41-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-221">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-222">**8**</span><span class="sxs-lookup"><span data-stu-id="e9a41-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-223">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e9a41-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-224">**9**</span><span class="sxs-lookup"><span data-stu-id="e9a41-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-225">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-226">**10**</span><span class="sxs-lookup"><span data-stu-id="e9a41-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-227">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-228">**11**</span><span class="sxs-lookup"><span data-stu-id="e9a41-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-229">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-230">**12**</span><span class="sxs-lookup"><span data-stu-id="e9a41-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-231">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-232">**13**</span><span class="sxs-lookup"><span data-stu-id="e9a41-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-233">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-234">**14**</span><span class="sxs-lookup"><span data-stu-id="e9a41-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-235">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-236">**15**</span><span class="sxs-lookup"><span data-stu-id="e9a41-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-237">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-238">**16**</span><span class="sxs-lookup"><span data-stu-id="e9a41-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-239">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-240">**17**</span><span class="sxs-lookup"><span data-stu-id="e9a41-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-241">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="e9a41-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-242">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="e9a41-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-243">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-244">**19**</span><span class="sxs-lookup"><span data-stu-id="e9a41-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-245">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-246">**20**</span><span class="sxs-lookup"><span data-stu-id="e9a41-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-247">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e9a41-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-248">**21**</span><span class="sxs-lookup"><span data-stu-id="e9a41-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-249">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-250">**22**</span><span class="sxs-lookup"><span data-stu-id="e9a41-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-251">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e9a41-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-252">**23**</span><span class="sxs-lookup"><span data-stu-id="e9a41-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-253">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9a41-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9a41-254">**24**</span><span class="sxs-lookup"><span data-stu-id="e9a41-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="e9a41-255">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="e9a41-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9a41-256">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9a41-256">Remarks</span></span>

<span data-ttu-id="e9a41-257">Dienste werden im Allgemeinen auf zwei Arten installiert: entweder als Teil der Installation des Betriebssystems oder mithilfe eines Installationsprogramms, das vom Dienst Entwickler bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a41-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="e9a41-258">Einige Dienste, insbesondere solche, die intern erstellt wurden, verfügen jedoch möglicherweise nicht über ein Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="e9a41-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="e9a41-259">In diesen Fällen können Sie die **Create** -Methode verwenden, um-Dienste Programm gesteuert zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e9a41-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="e9a41-260">Trotz des Namens erstellt die Create-Methode keinen Dienst. Es wird lediglich ein vorhandener Dienst installiert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="e9a41-261">Um diesen Befehl verwenden zu können, müssen Sie die ausführbare Dienst Datei auf einen Computer kopieren und dann **Create** verwenden, um den Dienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e9a41-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="e9a41-262">Die **Create** -Methode ähnelt der- [**Änderungs**](change-method-in-class-win32-service.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="e9a41-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="e9a41-263">In beiden Fällen werden die Eigenschaften des Dienes als Parameter an die-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e9a41-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="e9a41-264">Wie bei den Parametern, die mit der **Änderungs** Methode verwendet werden, ist die Reihenfolge, in der diese Parameter übermittelt werden, sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="e9a41-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="e9a41-265">Der *LoadOrderGroup* -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="e9a41-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="e9a41-266">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e9a41-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="e9a41-267">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e9a41-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="e9a41-268">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9a41-268">Examples</span></span>

<span data-ttu-id="e9a41-269">Mit dem folgenden VBScript wird ein Dienst mit dem Namen dbservice installiert.</span><span class="sxs-lookup"><span data-stu-id="e9a41-269">The following VBScript installs a service named DbService</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e9a41-270">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9a41-270">Requirements</span></span>



| <span data-ttu-id="e9a41-271">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9a41-271">Requirement</span></span> | <span data-ttu-id="e9a41-272">Wert</span><span class="sxs-lookup"><span data-stu-id="e9a41-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a41-273">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9a41-273">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a41-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9a41-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9a41-275">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9a41-275">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a41-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9a41-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9a41-277">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9a41-277">Namespace</span></span><br/>                | <span data-ttu-id="e9a41-278">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e9a41-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9a41-279">MOF</span><span class="sxs-lookup"><span data-stu-id="e9a41-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9a41-280"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e9a41-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9a41-281">DLL</span><span class="sxs-lookup"><span data-stu-id="e9a41-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9a41-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9a41-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a41-283">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9a41-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9a41-284">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9a41-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9a41-285">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="e9a41-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="e9a41-286">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="e9a41-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

