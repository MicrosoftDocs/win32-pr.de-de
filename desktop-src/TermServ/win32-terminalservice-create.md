---
title: Create-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Erstellt einen neuen-Systemdienst.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Create-Methode Remotedesktopdienste
- Create Method Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service Klasse Remotedesktopdienste, Methode erstellen
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
ms.openlocfilehash: be44d6c67e0d5bd6333f57c44cc44c25dc64e04a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477709"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="d929e-106">Create-Methode der Win32_Service-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="d929e-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="d929e-107">Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen-Systemdienst.</span><span class="sxs-lookup"><span data-stu-id="d929e-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="d929e-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d929e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d929e-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d929e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d929e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d929e-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d929e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d929e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d929e-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-113">Name des Dienstanbieter, der in der **Create** -Methode installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d929e-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="d929e-114">Die maximale Zeichen folgen Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d929e-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="d929e-115">Die Dienst Steuerungs Verwaltung behält die Groß-/Kleinschreibung der Zeichen bei. bei Dienstnamen vergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d929e-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="d929e-116">Schrägstriche (/) und Doppelte Rückstriche ( \) sind ungültige Dienstnamen Zeichen).</span><span class="sxs-lookup"><span data-stu-id="d929e-116">Forward-slashes (/) and double back-slashes (\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-117">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-118">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d929e-118">Display name of the service.</span></span> <span data-ttu-id="d929e-119">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d929e-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="d929e-120">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d929e-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="d929e-121">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d929e-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="d929e-122">Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d929e-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="d929e-123">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="d929e-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="d929e-124">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-125">Voll qualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="d929e-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="d929e-126">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="d929e-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="d929e-127">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-128">Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="d929e-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="d929e-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d929e-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-130">Kernel Treiber</span><span class="sxs-lookup"><span data-stu-id="d929e-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="d929e-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d929e-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-132">Datei System Treiber</span><span class="sxs-lookup"><span data-stu-id="d929e-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="d929e-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d929e-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-134">Adapter</span><span class="sxs-lookup"><span data-stu-id="d929e-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="d929e-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d929e-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-136">Erkennungs Treiber</span><span class="sxs-lookup"><span data-stu-id="d929e-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="d929e-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d929e-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-138">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="d929e-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="d929e-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d929e-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-140">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="d929e-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="d929e-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="d929e-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="d929e-142">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="d929e-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d929e-143">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-144">Der Schweregrad des Fehlers, wenn die **Create** -Methode nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d929e-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="d929e-145">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d929e-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="d929e-146">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d929e-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="d929e-147">0</span><span class="sxs-lookup"><span data-stu-id="d929e-147">0</span></span>
</dt> <dd>

<span data-ttu-id="d929e-148">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d929e-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-149">1</span><span class="sxs-lookup"><span data-stu-id="d929e-149">1</span></span>
</dt> <dd>

<span data-ttu-id="d929e-150">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d929e-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-151">2</span><span class="sxs-lookup"><span data-stu-id="d929e-151">2</span></span>
</dt> <dd>

<span data-ttu-id="d929e-152">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d929e-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-153">3</span><span class="sxs-lookup"><span data-stu-id="d929e-153">3</span></span>
</dt> <dd>

<span data-ttu-id="d929e-154">Das System versucht, mit einer guten Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d929e-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d929e-155">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-156">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d929e-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="d929e-157">Start</span><span class="sxs-lookup"><span data-stu-id="d929e-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="d929e-158">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="d929e-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="d929e-159">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="d929e-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-160">System</span><span class="sxs-lookup"><span data-stu-id="d929e-160">System</span></span>
</dt> <dd>

<span data-ttu-id="d929e-161">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="d929e-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="d929e-162">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="d929e-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-163">Automatisch</span><span class="sxs-lookup"><span data-stu-id="d929e-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="d929e-164">Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-165">Manuell</span><span class="sxs-lookup"><span data-stu-id="d929e-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="d929e-166">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](win32-terminalservice-startservice.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="d929e-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-167">Disabled</span><span class="sxs-lookup"><span data-stu-id="d929e-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="d929e-168">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d929e-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d929e-169">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-170">**True** gibt an, dass der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="d929e-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-171">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-172">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-172">Account name under which the service runs.</span></span> <span data-ttu-id="d929e-173">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder "Benutzer Prinzipal Name (UPN) Format ()" aufweisen Username@DomainName .</span><span class="sxs-lookup"><span data-stu-id="d929e-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="d929e-174">Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="d929e-175">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d929e-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="d929e-176">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="d929e-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="d929e-177">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d929e-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="d929e-178">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d929e-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="d929e-179">Beispiel: dwdom- \\ Administrator.</span><span class="sxs-lookup"><span data-stu-id="d929e-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-180">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-181">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="d929e-182">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="d929e-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="d929e-183">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="d929e-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-184">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-185">Der dem neuen Dienst zugeordnete Gruppenname.</span><span class="sxs-lookup"><span data-stu-id="d929e-185">Group name associated with the new service.</span></span> <span data-ttu-id="d929e-186">Lade Auftrags Gruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d929e-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="d929e-187">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge verweist, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d929e-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="d929e-188">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d929e-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="d929e-189">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="d929e-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="d929e-190">Die Registrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="d929e-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="d929e-191">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="d929e-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="d929e-192">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-193">Array von Gruppen für die Auslastungs Anordnung, die vor diesem Dienst gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d929e-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="d929e-194">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="d929e-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d929e-195">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="d929e-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d929e-196">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d929e-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d929e-197">Gruppennamen muss der **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um ihn von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="d929e-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="d929e-198">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="d929e-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-199">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d929e-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d929e-200">Ein Array, das Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d929e-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="d929e-201">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="d929e-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d929e-202">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="d929e-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d929e-203">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d929e-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d929e-204">Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d929e-205">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d929e-205">Return value</span></span>

<span data-ttu-id="d929e-206">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d929e-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="d929e-207">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d929e-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d929e-208">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d929e-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d929e-209">**0**</span><span class="sxs-lookup"><span data-stu-id="d929e-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-210">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d929e-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-211">**1**</span><span class="sxs-lookup"><span data-stu-id="d929e-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-212">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d929e-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-213">**2**</span><span class="sxs-lookup"><span data-stu-id="d929e-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-214">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="d929e-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-215">**3**</span><span class="sxs-lookup"><span data-stu-id="d929e-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-216">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d929e-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-217">**4**</span><span class="sxs-lookup"><span data-stu-id="d929e-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-218">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="d929e-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-219">**5**</span><span class="sxs-lookup"><span data-stu-id="d929e-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-220">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts (**State** -Eigenschaft der [**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice) -Klasse) gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="d929e-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-221">**6**</span><span class="sxs-lookup"><span data-stu-id="d929e-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-222">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d929e-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-223">**7**</span><span class="sxs-lookup"><span data-stu-id="d929e-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-224">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="d929e-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-225">**8**</span><span class="sxs-lookup"><span data-stu-id="d929e-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-226">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d929e-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-227">**9**</span><span class="sxs-lookup"><span data-stu-id="d929e-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-228">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d929e-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-229">**10**</span><span class="sxs-lookup"><span data-stu-id="d929e-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-230">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d929e-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-231">**11**</span><span class="sxs-lookup"><span data-stu-id="d929e-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-232">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d929e-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-233">**12**</span><span class="sxs-lookup"><span data-stu-id="d929e-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-234">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d929e-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-235">**13**</span><span class="sxs-lookup"><span data-stu-id="d929e-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-236">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-237">**14**</span><span class="sxs-lookup"><span data-stu-id="d929e-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-238">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d929e-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-239">**15**</span><span class="sxs-lookup"><span data-stu-id="d929e-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-240">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="d929e-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-241">**16**</span><span class="sxs-lookup"><span data-stu-id="d929e-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-242">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d929e-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-243">**17**</span><span class="sxs-lookup"><span data-stu-id="d929e-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-244">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="d929e-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-245">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="d929e-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-246">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-247">**19**</span><span class="sxs-lookup"><span data-stu-id="d929e-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-248">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d929e-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-249">**20**</span><span class="sxs-lookup"><span data-stu-id="d929e-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-250">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d929e-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-251">**21**</span><span class="sxs-lookup"><span data-stu-id="d929e-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-252">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d929e-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-253">**22**</span><span class="sxs-lookup"><span data-stu-id="d929e-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-254">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d929e-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-255">**23**</span><span class="sxs-lookup"><span data-stu-id="d929e-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-256">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d929e-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d929e-257">**24**</span><span class="sxs-lookup"><span data-stu-id="d929e-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d929e-258">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="d929e-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d929e-259">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d929e-259">Remarks</span></span>

<span data-ttu-id="d929e-260">Dienste werden im Allgemeinen auf zwei Arten installiert: entweder als Teil der Installation des Betriebssystems oder mithilfe eines Installationsprogramms, das vom Dienst Entwickler bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d929e-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="d929e-261">Einige Dienste, insbesondere solche, die intern erstellt wurden, verfügen jedoch möglicherweise nicht über ein Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="d929e-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="d929e-262">In diesen Fällen können Sie die **Create** -Methode verwenden, um-Dienste Programm gesteuert zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d929e-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="d929e-263">Trotz des Namens erstellt die Create-Methode keinen Dienst. Es wird lediglich ein vorhandener Dienst installiert.</span><span class="sxs-lookup"><span data-stu-id="d929e-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="d929e-264">Um diesen Befehl verwenden zu können, müssen Sie die ausführbare Dienst Datei auf einen Computer kopieren und dann **Create** verwenden, um den Dienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d929e-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="d929e-265">Die **Create** -Methode ähnelt der- [**Änderungs**](win32-terminalservice-change.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="d929e-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="d929e-266">In beiden Fällen werden die Eigenschaften des Dienes als Parameter an die-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d929e-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="d929e-267">Wie bei den Parametern, die mit der **Änderungs** Methode verwendet werden, ist die Reihenfolge, in der diese Parameter übermittelt werden, sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="d929e-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="d929e-268">Der *LoadOrderGroup* -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="d929e-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="d929e-269">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d929e-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="d929e-270">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d929e-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d929e-271">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d929e-271">Requirements</span></span>



| <span data-ttu-id="d929e-272">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d929e-272">Requirement</span></span> | <span data-ttu-id="d929e-273">Wert</span><span class="sxs-lookup"><span data-stu-id="d929e-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d929e-274">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d929e-274">Minimum supported client</span></span><br/> | <span data-ttu-id="d929e-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d929e-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d929e-276">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d929e-276">Minimum supported server</span></span><br/> | <span data-ttu-id="d929e-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d929e-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d929e-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="d929e-278">Namespace</span></span><br/>                | <span data-ttu-id="d929e-279">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d929e-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d929e-280">MOF</span><span class="sxs-lookup"><span data-stu-id="d929e-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d929e-281"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d929e-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d929e-282">DLL</span><span class="sxs-lookup"><span data-stu-id="d929e-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d929e-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d929e-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d929e-284">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d929e-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d929e-285">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="d929e-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="d929e-286">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="d929e-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="d929e-287">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="d929e-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="d929e-288">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="d929e-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

