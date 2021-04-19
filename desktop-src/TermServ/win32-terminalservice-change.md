---
title: Change-Methode der Win32_Service-Klasse (mbnapi. h)
description: Ändert einen Win32 \_ Terminalservice.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Änderungs Methode Remotedesktopdienste
- Change-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, Methode ändern
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4514d89e47ded60550a28303d0f04e227211e3a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106355243"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="3338a-106">Change-Methode der Win32_Service-Klasse (mbnapi. h)-Terminalservice</span><span class="sxs-lookup"><span data-stu-id="3338a-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="3338a-107">Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert einen [**Win32 \_ Terminalservice**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="3338a-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="3338a-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3338a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3338a-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3338a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3338a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3338a-110">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="3338a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3338a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3338a-112">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-113">Der Anzeigename des Diensts</span><span class="sxs-lookup"><span data-stu-id="3338a-113">The display name of the service.</span></span> <span data-ttu-id="3338a-114">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3338a-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="3338a-115">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3338a-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="3338a-116">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="3338a-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="3338a-117">Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3338a-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="3338a-118">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="3338a-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="3338a-119">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-120">Der voll qualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert, z. b \\ . "SystemRoot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="3338a-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="3338a-121">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-122">Der Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="3338a-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="3338a-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3338a-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-124">Kernel Treiber</span><span class="sxs-lookup"><span data-stu-id="3338a-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="3338a-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3338a-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-126">Datei System Treiber</span><span class="sxs-lookup"><span data-stu-id="3338a-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="3338a-127">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="3338a-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-128">Adapter</span><span class="sxs-lookup"><span data-stu-id="3338a-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="3338a-129">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="3338a-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-130">Erkennungs Treiber</span><span class="sxs-lookup"><span data-stu-id="3338a-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="3338a-131">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="3338a-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-132">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="3338a-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="3338a-133">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="3338a-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-134">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="3338a-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="3338a-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="3338a-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="3338a-136">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="3338a-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3338a-137">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-138">Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3338a-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="3338a-139">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3338a-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="3338a-140">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3338a-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="3338a-141">0</span><span class="sxs-lookup"><span data-stu-id="3338a-141">0</span></span>
</dt> <dd>

<span data-ttu-id="3338a-142">**Ignore** (Ignorieren):</span><span class="sxs-lookup"><span data-stu-id="3338a-142">**Ignore**.</span></span> <span data-ttu-id="3338a-143">Der Startvorgang fortgesetzt</span><span class="sxs-lookup"><span data-stu-id="3338a-143">Startup continues.</span></span> <span data-ttu-id="3338a-144">Der Benutzer erhält keine Benachrichtigung, dass der Dienst fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3338a-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-145">1</span><span class="sxs-lookup"><span data-stu-id="3338a-145">1</span></span>
</dt> <dd>

<span data-ttu-id="3338a-146">**Normaler.**</span><span class="sxs-lookup"><span data-stu-id="3338a-146">**Normal.**</span></span> <span data-ttu-id="3338a-147">Der Startvorgang fortgesetzt</span><span class="sxs-lookup"><span data-stu-id="3338a-147">Startup continues.</span></span> <span data-ttu-id="3338a-148">Bevor der Benutzer sich anmeldet, erhält der Benutzer die Benachrichtigung, dass mindestens ein Dienst oder ein Gerät während des Starts fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3338a-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="3338a-149">2</span><span class="sxs-lookup"><span data-stu-id="3338a-149">2</span></span>
</dt> <dd>

<span data-ttu-id="3338a-150">**Starkem.**</span><span class="sxs-lookup"><span data-stu-id="3338a-150">**Severe.**</span></span> <span data-ttu-id="3338a-151">Der Computer versucht, mit der zuletzt bekannten guten Konfiguration neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="3338a-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="3338a-152">Wenn der Dienst erneut ausfällt, wird der Startvorgang fortgesetzt, und der Benutzer erhält eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3338a-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-153">3</span><span class="sxs-lookup"><span data-stu-id="3338a-153">3</span></span>
</dt> <dd>

<span data-ttu-id="3338a-154">**Kritisch.**</span><span class="sxs-lookup"><span data-stu-id="3338a-154">**Critical.**</span></span> <span data-ttu-id="3338a-155">Der Computer versucht, mit der zuletzt bekannten guten Konfiguration neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="3338a-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="3338a-156">Wenn der Dienst erneut ausfällt, wird der Startvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="3338a-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3338a-157">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-158">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3338a-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="3338a-159">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="3338a-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="3338a-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Starten**</span><span class="sxs-lookup"><span data-stu-id="3338a-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="3338a-161">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="3338a-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="3338a-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Anlage**</span><span class="sxs-lookup"><span data-stu-id="3338a-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="3338a-163">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="3338a-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="3338a-164">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="3338a-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="3338a-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**</span><span class="sxs-lookup"><span data-stu-id="3338a-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="3338a-166">Der Dienst wird vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="3338a-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="3338a-167">Autostart-Dienste werden gestartet, bevor sich ein Benutzer am Computer anmeldet und ausgeführt wird, selbst wenn sich kein Benutzer am Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="3338a-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="3338a-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**</span><span class="sxs-lookup"><span data-stu-id="3338a-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="3338a-169">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](win32-terminalservice-startservice.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="3338a-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="3338a-170">Obwohl manuelle Dienste speziell von einem Benutzer (oder einem Skript) gestartet werden müssen, werden Sie weiterhin ausgeführt, selbst wenn sich der Benutzer abmeldet.</span><span class="sxs-lookup"><span data-stu-id="3338a-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="3338a-171">Manuelle Dienste werden häufig als Bedarfs gesteuerte Dienste bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3338a-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3338a-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="3338a-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="3338a-173">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3338a-173">Service that can no longer be started.</span></span> <span data-ttu-id="3338a-174">Um einen deaktivierten Dienst zu starten, müssen Sie zuerst die Startoption entweder in Auto oder manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="3338a-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3338a-175">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-176">**True** gibt an, dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="3338a-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-177">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-178">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-178">Account name the service runs under.</span></span> <span data-ttu-id="3338a-179">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name Benutzername" oder "" aufweisen \\ . \\ User.</span><span class="sxs-lookup"><span data-stu-id="3338a-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="3338a-180">Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3338a-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="3338a-181">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="3338a-182">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3338a-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="3338a-183">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="3338a-184">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System auf Basis des Dienst namens erstellt wird, z. b. "dwdom \\ Admin".</span><span class="sxs-lookup"><span data-stu-id="3338a-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="3338a-185">Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..</span><span class="sxs-lookup"><span data-stu-id="3338a-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-186">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-187">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="3338a-188">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="3338a-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="3338a-189">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="3338a-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="3338a-190">Wenn ein Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk auf ein lokales System geändert wird, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3338a-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="3338a-191">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-192">Der Gruppenname, dem er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3338a-192">Group name that it is associated with.</span></span> <span data-ttu-id="3338a-193">Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="3338a-194">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3338a-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="3338a-195">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="3338a-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="3338a-196">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="3338a-197">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="3338a-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="3338a-198">Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="3338a-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="3338a-199">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="3338a-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="3338a-200">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-201">Liste der Lade Gruppen, die vor dem Start dieses Dienstanbieter gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3338a-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="3338a-202">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="3338a-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="3338a-203">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="3338a-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="3338a-204">Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, damit Sie von Dienstnamen unterschieden werden, weil Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="3338a-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="3338a-205">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="3338a-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-206">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3338a-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3338a-207">Liste mit den Namen der Dienste, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3338a-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="3338a-208">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="3338a-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="3338a-209">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="3338a-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="3338a-210">Die Abhängigkeit von einem Dienst gibt an, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3338a-211">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3338a-211">Return value</span></span>

<span data-ttu-id="3338a-212">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3338a-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3338a-213">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3338a-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3338a-214">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3338a-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3338a-215">**0**</span><span class="sxs-lookup"><span data-stu-id="3338a-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-216">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3338a-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-217">**1**</span><span class="sxs-lookup"><span data-stu-id="3338a-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-218">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3338a-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-219">**2**</span><span class="sxs-lookup"><span data-stu-id="3338a-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-220">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="3338a-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-221">**3**</span><span class="sxs-lookup"><span data-stu-id="3338a-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-222">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="3338a-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-223">**4**</span><span class="sxs-lookup"><span data-stu-id="3338a-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-224">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="3338a-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-225">**5**</span><span class="sxs-lookup"><span data-stu-id="3338a-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-226">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="3338a-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-227">**6**</span><span class="sxs-lookup"><span data-stu-id="3338a-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-228">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="3338a-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-229">**7**</span><span class="sxs-lookup"><span data-stu-id="3338a-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-230">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="3338a-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-231">**8**</span><span class="sxs-lookup"><span data-stu-id="3338a-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-232">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3338a-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-233">**9**</span><span class="sxs-lookup"><span data-stu-id="3338a-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-234">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="3338a-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-235">**10**</span><span class="sxs-lookup"><span data-stu-id="3338a-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-236">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3338a-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-237">**11**</span><span class="sxs-lookup"><span data-stu-id="3338a-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-238">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="3338a-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-239">**12**</span><span class="sxs-lookup"><span data-stu-id="3338a-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-240">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="3338a-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-241">**13**</span><span class="sxs-lookup"><span data-stu-id="3338a-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-242">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-243">**14**</span><span class="sxs-lookup"><span data-stu-id="3338a-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-244">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3338a-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-245">**15**</span><span class="sxs-lookup"><span data-stu-id="3338a-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-246">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-247">**16**</span><span class="sxs-lookup"><span data-stu-id="3338a-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-248">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="3338a-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-249">**17**</span><span class="sxs-lookup"><span data-stu-id="3338a-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-250">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="3338a-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-251">**Jahren**</span><span class="sxs-lookup"><span data-stu-id="3338a-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-252">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-253">**19**</span><span class="sxs-lookup"><span data-stu-id="3338a-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-254">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3338a-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-255">**20**</span><span class="sxs-lookup"><span data-stu-id="3338a-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-256">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3338a-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-257">**21**</span><span class="sxs-lookup"><span data-stu-id="3338a-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-258">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3338a-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-259">**22**</span><span class="sxs-lookup"><span data-stu-id="3338a-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-260">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3338a-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-261">**23**</span><span class="sxs-lookup"><span data-stu-id="3338a-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-262">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3338a-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3338a-263">**24**</span><span class="sxs-lookup"><span data-stu-id="3338a-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3338a-264">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="3338a-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3338a-265">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3338a-265">Remarks</span></span>

<span data-ttu-id="3338a-266">Wenn ein Computer gestartet wird, werden alle Autostart-Dienste ebenfalls gestartet.</span><span class="sxs-lookup"><span data-stu-id="3338a-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="3338a-267">Gelegentlich kann es vorkommen, dass einer dieser Dienste nicht zusammen mit dem Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="3338a-268">Wenn ein Dienst beim Systemstart fehlschlägt, führt der Computer auf der Grundlage des Werts des Dienst Fehler-Steuerungs Codes Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="3338a-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="3338a-269">die meisten Dienste werden mithilfe des normalen fehlersteuerungs Codes installiert.</span><span class="sxs-lookup"><span data-stu-id="3338a-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="3338a-270">Einige Ausnahmen, die mit dem Fehlercode ignorieren installiert werden, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3338a-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="3338a-271">Dateireplikationsdienst</span><span class="sxs-lookup"><span data-stu-id="3338a-271">File Replication Service</span></span>
-   <span data-ttu-id="3338a-272">Smartcard</span><span class="sxs-lookup"><span data-stu-id="3338a-272">Smart Card</span></span>
-   <span data-ttu-id="3338a-273">Sekundäre Anmeldung</span><span class="sxs-lookup"><span data-stu-id="3338a-273">Secondary Logon</span></span>
-   <span data-ttu-id="3338a-274">WMI</span><span class="sxs-lookup"><span data-stu-id="3338a-274">WMI</span></span>

<span data-ttu-id="3338a-275">Für die Dienste, die mit dem Fehlercode ignorieren installiert werden, erhält der Benutzer keine Benachrichtigung, dass der Dienst fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3338a-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="3338a-276">Wenn Sie die Benachrichtigung auf dem Bildschirm bevorzugen, dass ein Dienst nicht gestartet werden konnte, können Sie den Fehlercode mithilfe von WMI ändern.</span><span class="sxs-lookup"><span data-stu-id="3338a-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="3338a-277">Fehler Steuerungs Codes gelten nur für den Computer Start. Es werden keine Fehlercodes verwendet, wenn Sie einen Dienst nach dem Ausführen des Computers abbrechen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="3338a-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="3338a-278">Gelegentlich müssen Sie möglicherweise das Konto ändern, unter dem ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="3338a-279">Beispielsweise können Sie einen Dienst unter einem Administrator Konto ausführen.</span><span class="sxs-lookup"><span data-stu-id="3338a-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="3338a-280">Da dadurch ein Sicherheitsrisiko entstehen kann, können Sie den Dienst zu einem Konto mit weniger Berechtigungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="3338a-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="3338a-281">Möglicherweise verfügen Sie auch über Dienste, die unter einem Konto ausgeführt werden, das gelöscht werden soll, oder Sie möchten sicherstellen, dass bestimmte Dienste auf allen Servern unter bestimmten Konten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="3338a-282">Sie können die **Change** -Methode der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse verwenden, um Dienste so zu konfigurieren, dass Sie unter einem angegebenen Benutzerkonto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="3338a-283">Wenn Sie ein Konto auswählen, beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3338a-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="3338a-284">Das Konto, das als Dienst Konto verwendet wird, muss über die Berechtigung verfügen, sich als Dienst anzumelden.</span><span class="sxs-lookup"><span data-stu-id="3338a-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="3338a-285">Dieses Recht kann mithilfe von Gruppenrichtlinie erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="3338a-286">Das Konto, das als Dienst Konto verwendet wird, sollte nicht Mitglied einer lokalen Gruppe, einer Domäne oder einer Organisations Administratoren Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="3338a-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="3338a-287">Jede Instanz eines Dienstanbieter sollte unter einem eindeutigen Benutzerkonto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="3338a-288">Dies bietet zusätzliche Sicherheit und ermöglicht die Überwachung einzelner Dienst Instanzen.</span><span class="sxs-lookup"><span data-stu-id="3338a-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="3338a-289">Wenn der Dienst interaktiv ist, muss der Dienst unter dem Konto "LocalSystem" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="3338a-290">"LocalSystem" ist erforderlich, da jeweils nur eine Fenster Station (WinSta0) sichtbar und interaktiv sein kann.</span><span class="sxs-lookup"><span data-stu-id="3338a-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="3338a-291">Wenn ein Dienst unter einem anderen Konto als "LocalSystem" ausgeführt wird, wird er auf der Standard Station des Dienst-0x03e7 $-Fensters ausgeführt, bei dem es sich \\ um ein unsichtbares Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="3338a-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="3338a-292">Dienste, die in dieser Fenster Station ausgeführt werden, können keine Eingabe-oder Anzeige Ausgabe empfangen.</span><span class="sxs-lookup"><span data-stu-id="3338a-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="3338a-293">Wenn Sie ein Konto einem Dienst zuweisen, benötigt der SCM das richtige Kennwort für dieses Konto, bevor die Zuweisung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="3338a-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="3338a-294">Wenn Sie ein falsches Kennwort angeben, lehnt der SCM das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3338a-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="3338a-295">Wenn Sie ein Dienst Konto mit dem Konto "LocalSystem", "LocalService" oder "Network Service" konfigurieren, müssen Sie kein Konto Kennwort angeben, da diese Konten keine Kenn Wörter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3338a-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="3338a-296">Der SCM speichert das Konto Kennwort in der Dienst Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3338a-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="3338a-297">Nachdem das Kennwort zugewiesen wurde, stellt der SCM jedoch nicht sicher, dass das Kennwort, das in der Dienst Datenbank gespeichert ist, und das Kennwort, das dem Benutzerkonto in zugewiesen ist, weiterhin mit der Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3338a-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="3338a-298">Folglich könnte eine ähnliche Situation wie die folgende auftreten:</span><span class="sxs-lookup"><span data-stu-id="3338a-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="3338a-299">. Sie konfigurieren einen Dienst, der unter einem bestimmten Benutzerkonto ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3338a-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="3338a-300">Der Dienst wird mit dem aktuellen Konto Kennwort unter diesem Konto gestartet.</span><span class="sxs-lookup"><span data-stu-id="3338a-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="3338a-301">Sie ändern das Kennwort für das Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="3338a-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="3338a-302">Der Dienst wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3338a-302">The service continues to run.</span></span> <span data-ttu-id="3338a-303">Wenn der Dienst jedoch beendet wird, können Sie ihn nicht neu starten, da der SCM weiterhin das alte, ungültige Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="3338a-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="3338a-304">Wenn Sie das Kennwort in Active Directory ändern, wird das in der Dienst Datenbank gespeicherte Kennwort nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="3338a-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="3338a-305">Wenn Sie Dienste unter regulären Benutzerkonten ausführen, müssen Sie diese Dienst Kennwörter jedes Mal aktualisieren, wenn das Kennwort des Benutzerkontos geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3338a-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="3338a-306">Dies kann besonders zeitaufwändig sein, wenn Sie nicht sicher sind, welche Dienste unter diesem Konto ausgeführt werden oder welche Computer über Dienste verfügen, die unter diesem Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3338a-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="3338a-307">Glücklicherweise können Sie WMI verwenden, um die Dienst Konten auf allen Computern zu überprüfen und ggf. das Kennwort des Dienst Kontos zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3338a-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="3338a-308">Der [**Win32 \_ LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) -Parameter stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="3338a-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="3338a-309">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="3338a-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="3338a-310">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="3338a-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="3338a-311">Um einen Dienst von einem Netzwerkdienst in ein lokales System zu ändern, müssen die Parameter " *StartName* " und " *startpassword* " die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3338a-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="3338a-312">Um einen Dienst von einem lokalen Systemdienst in ein Netzwerk zu ändern, müssen die Parameter " *StartName* " und " *startpassword* " die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3338a-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="3338a-313">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3338a-313">Examples</span></span>

<span data-ttu-id="3338a-314">Das folgende VBScript ändert das Dienst Konto für Dienste von der Ausführung unter einem angegebenen Benutzerkonto in "LocalSystem".</span><span class="sxs-lookup"><span data-stu-id="3338a-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="3338a-315">Das folgende VBScript ändert das Dienst Konto Kennwort für alle Skripts, die unter "nettsvc" ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="3338a-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="3338a-316">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3338a-316">Requirements</span></span>



| <span data-ttu-id="3338a-317">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3338a-317">Requirement</span></span> | <span data-ttu-id="3338a-318">Wert</span><span class="sxs-lookup"><span data-stu-id="3338a-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3338a-319">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3338a-319">Minimum supported client</span></span><br/> | <span data-ttu-id="3338a-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3338a-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3338a-321">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3338a-321">Minimum supported server</span></span><br/> | <span data-ttu-id="3338a-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3338a-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3338a-323">Namespace</span><span class="sxs-lookup"><span data-stu-id="3338a-323">Namespace</span></span><br/>                | <span data-ttu-id="3338a-324">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3338a-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3338a-325">Header</span><span class="sxs-lookup"><span data-stu-id="3338a-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="3338a-326"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3338a-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="3338a-327">MOF</span><span class="sxs-lookup"><span data-stu-id="3338a-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3338a-328"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3338a-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3338a-329">DLL</span><span class="sxs-lookup"><span data-stu-id="3338a-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3338a-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3338a-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3338a-331">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3338a-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3338a-332">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="3338a-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="3338a-333">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="3338a-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="3338a-334">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="3338a-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="3338a-335">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="3338a-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

