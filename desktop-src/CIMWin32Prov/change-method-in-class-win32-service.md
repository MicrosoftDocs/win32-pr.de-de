---
description: Ändert einen Win32- \_ Dienst.
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Change-Methode der Win32_Service-Klasse (mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523923"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="e05d7-103">Change-Methode der Win32_Service-Klasse (mbnapi. h)</span><span class="sxs-lookup"><span data-stu-id="e05d7-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="e05d7-104">Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert einen [**Win32- \_ Dienst**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="e05d7-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="e05d7-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e05d7-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e05d7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e05d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e05d7-107">Syntax</span></span>


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
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="e05d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e05d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05d7-109">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-110">Der Anzeigename des Diensts</span><span class="sxs-lookup"><span data-stu-id="e05d7-110">The display name of the service.</span></span> <span data-ttu-id="e05d7-111">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="e05d7-112">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="e05d7-113">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="e05d7-114">Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e05d7-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="e05d7-115">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="e05d7-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-116">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-117">Der voll qualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert, z. b \\ . "SystemRoot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="e05d7-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-118">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-119">Der Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="e05d7-120">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e05d7-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-121">Kernel Treiber</span><span class="sxs-lookup"><span data-stu-id="e05d7-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-122">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="e05d7-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-123">Datei System Treiber</span><span class="sxs-lookup"><span data-stu-id="e05d7-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-124">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e05d7-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-125">Adapter</span><span class="sxs-lookup"><span data-stu-id="e05d7-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-126">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="e05d7-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-127">Erkennungs Treiber</span><span class="sxs-lookup"><span data-stu-id="e05d7-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="e05d7-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-129">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="e05d7-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-130">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e05d7-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-131">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="e05d7-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="e05d7-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-133">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="e05d7-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e05d7-134">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-135">Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e05d7-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="e05d7-136">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="e05d7-137">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="e05d7-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** (0)</span><span class="sxs-lookup"><span data-stu-id="e05d7-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e05d7-139">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="e05d7-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="e05d7-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e05d7-141">Normal.</span><span class="sxs-lookup"><span data-stu-id="e05d7-141">Normal.</span></span> <span data-ttu-id="e05d7-142">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="e05d7-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)</span><span class="sxs-lookup"><span data-stu-id="e05d7-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e05d7-144">Das System wird mit der letzten guten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e05d7-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="e05d7-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e05d7-146">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e05d7-147">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-148">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e05d7-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="e05d7-149">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="e05d7-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="e05d7-150">Start</span><span class="sxs-lookup"><span data-stu-id="e05d7-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-151">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e05d7-152">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="e05d7-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-153">System</span><span class="sxs-lookup"><span data-stu-id="e05d7-153">System</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-154">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e05d7-155">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="e05d7-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-156">Automatisch</span><span class="sxs-lookup"><span data-stu-id="e05d7-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-157">Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-158">Manuell</span><span class="sxs-lookup"><span data-stu-id="e05d7-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-159">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="e05d7-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-160">Disabled</span><span class="sxs-lookup"><span data-stu-id="e05d7-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-161">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e05d7-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e05d7-162">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-163">**True** gibt an, dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="e05d7-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-164">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-165">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-165">Account name the service runs under.</span></span> <span data-ttu-id="e05d7-166">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name Benutzername" oder "" aufweisen \\ . \\ User.</span><span class="sxs-lookup"><span data-stu-id="e05d7-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="e05d7-167">Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="e05d7-168">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="e05d7-169">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="e05d7-170">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="e05d7-171">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System auf Basis des Dienst namens erstellt wird, z. b. "dwdom \\ Admin".</span><span class="sxs-lookup"><span data-stu-id="e05d7-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="e05d7-172">Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..</span><span class="sxs-lookup"><span data-stu-id="e05d7-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-173">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-174">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="e05d7-175">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e05d7-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="e05d7-176">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="e05d7-177">Wenn ein Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk auf ein lokales System geändert wird, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e05d7-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="e05d7-178">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-179">Der Gruppenname, dem er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e05d7-179">Group name that it is associated with.</span></span> <span data-ttu-id="e05d7-180">Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="e05d7-181">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e05d7-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="e05d7-182">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="e05d7-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="e05d7-183">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="e05d7-184">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="e05d7-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="e05d7-185">Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="e05d7-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="e05d7-186">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="e05d7-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-187">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-188">Liste der Lade Gruppen, die vor dem Start dieses Dienstanbieter gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="e05d7-189">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="e05d7-190">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="e05d7-191">Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, damit Sie von Dienstnamen unterschieden werden, weil Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="e05d7-192">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-193">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e05d7-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-194">Liste mit den Namen der Dienste, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="e05d7-195">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="e05d7-196">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="e05d7-197">Die Abhängigkeit von einem Dienst gibt an, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05d7-198">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e05d7-198">Return value</span></span>

<span data-ttu-id="e05d7-199">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e05d7-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="e05d7-200">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e05d7-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e05d7-201">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e05d7-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e05d7-202">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="e05d7-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-203">0</span><span class="sxs-lookup"><span data-stu-id="e05d7-203">0</span></span>

<span data-ttu-id="e05d7-204">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-205">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="e05d7-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-206">1</span><span class="sxs-lookup"><span data-stu-id="e05d7-206">1</span></span>

<span data-ttu-id="e05d7-207">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-208">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="e05d7-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-209">2</span><span class="sxs-lookup"><span data-stu-id="e05d7-209">2</span></span>

<span data-ttu-id="e05d7-210">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="e05d7-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-211">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="e05d7-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-212">3</span><span class="sxs-lookup"><span data-stu-id="e05d7-212">3</span></span>

<span data-ttu-id="e05d7-213">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e05d7-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-214">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-215">4</span><span class="sxs-lookup"><span data-stu-id="e05d7-215">4</span></span>

<span data-ttu-id="e05d7-216">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="e05d7-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-217">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-218">5</span><span class="sxs-lookup"><span data-stu-id="e05d7-218">5</span></span>

<span data-ttu-id="e05d7-219">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="e05d7-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-220">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="e05d7-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-221">6</span><span class="sxs-lookup"><span data-stu-id="e05d7-221">6</span></span>

<span data-ttu-id="e05d7-222">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-223">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="e05d7-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-224">7</span><span class="sxs-lookup"><span data-stu-id="e05d7-224">7</span></span>

<span data-ttu-id="e05d7-225">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-226">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-227">8</span><span class="sxs-lookup"><span data-stu-id="e05d7-227">8</span></span>

<span data-ttu-id="e05d7-228">Unbekannter Fehler beim Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e05d7-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-229">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="e05d7-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-230">9</span><span class="sxs-lookup"><span data-stu-id="e05d7-230">9</span></span>

<span data-ttu-id="e05d7-231">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-232">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-233">10</span><span class="sxs-lookup"><span data-stu-id="e05d7-233">10</span></span>

<span data-ttu-id="e05d7-234">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-235">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="e05d7-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-236">11</span><span class="sxs-lookup"><span data-stu-id="e05d7-236">11</span></span>

<span data-ttu-id="e05d7-237">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-238">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="e05d7-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-239">12</span><span class="sxs-lookup"><span data-stu-id="e05d7-239">12</span></span>

<span data-ttu-id="e05d7-240">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-241">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="e05d7-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-242">13</span><span class="sxs-lookup"><span data-stu-id="e05d7-242">13</span></span>

<span data-ttu-id="e05d7-243">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-244">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="e05d7-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-245">14</span><span class="sxs-lookup"><span data-stu-id="e05d7-245">14</span></span>

<span data-ttu-id="e05d7-246">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-247">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="e05d7-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-248">15</span><span class="sxs-lookup"><span data-stu-id="e05d7-248">15</span></span>

<span data-ttu-id="e05d7-249">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-250">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-251">16</span><span class="sxs-lookup"><span data-stu-id="e05d7-251">16</span></span>

<span data-ttu-id="e05d7-252">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-253">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="e05d7-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-254">17</span><span class="sxs-lookup"><span data-stu-id="e05d7-254">17</span></span>

<span data-ttu-id="e05d7-255">Der Dienst hat keinen Ausführungs Thread.</span><span class="sxs-lookup"><span data-stu-id="e05d7-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-256">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="e05d7-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-257">18</span><span class="sxs-lookup"><span data-stu-id="e05d7-257">18</span></span>

<span data-ttu-id="e05d7-258">Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-259">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="e05d7-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-260">19</span><span class="sxs-lookup"><span data-stu-id="e05d7-260">19</span></span>

<span data-ttu-id="e05d7-261">Ein Dienst wird unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-262">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="e05d7-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-263">20</span><span class="sxs-lookup"><span data-stu-id="e05d7-263">20</span></span>

<span data-ttu-id="e05d7-264">Der Dienst Name enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-265">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-266">21</span><span class="sxs-lookup"><span data-stu-id="e05d7-266">21</span></span>

<span data-ttu-id="e05d7-267">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-268">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-269">22</span><span class="sxs-lookup"><span data-stu-id="e05d7-269">22</span></span>

<span data-ttu-id="e05d7-270">Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e05d7-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-271">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="e05d7-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-272">23</span><span class="sxs-lookup"><span data-stu-id="e05d7-272">23</span></span>

<span data-ttu-id="e05d7-273">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-274">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="e05d7-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-275">24</span><span class="sxs-lookup"><span data-stu-id="e05d7-275">24</span></span>

<span data-ttu-id="e05d7-276">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="e05d7-277">**Andere**</span><span class="sxs-lookup"><span data-stu-id="e05d7-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e05d7-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="e05d7-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e05d7-279">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e05d7-279">Remarks</span></span>

<span data-ttu-id="e05d7-280">Wenn ein Computer gestartet wird, werden alle Autostart-Dienste ebenfalls gestartet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="e05d7-281">Gelegentlich kann es vorkommen, dass einer dieser Dienste nicht zusammen mit dem Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="e05d7-282">Wenn ein Dienst beim Systemstart fehlschlägt, führt der Computer auf der Grundlage des Werts des Dienst Fehler-Steuerungs Codes Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="e05d7-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="e05d7-283">die meisten Dienste werden mithilfe des normalen fehlersteuerungs Codes installiert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="e05d7-284">Einige Ausnahmen, die mit dem Fehlercode ignorieren installiert werden, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e05d7-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="e05d7-285">Dateireplikationsdienst</span><span class="sxs-lookup"><span data-stu-id="e05d7-285">File Replication Service</span></span>
-   <span data-ttu-id="e05d7-286">Smartcard</span><span class="sxs-lookup"><span data-stu-id="e05d7-286">Smart Card</span></span>
-   <span data-ttu-id="e05d7-287">Sekundäre Anmeldung</span><span class="sxs-lookup"><span data-stu-id="e05d7-287">Secondary Logon</span></span>
-   <span data-ttu-id="e05d7-288">WMI</span><span class="sxs-lookup"><span data-stu-id="e05d7-288">WMI</span></span>

<span data-ttu-id="e05d7-289">Für die Dienste, die mit dem Fehlercode ignorieren installiert werden, erhält der Benutzer keine Benachrichtigung, dass der Dienst fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e05d7-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="e05d7-290">Wenn Sie die Benachrichtigung auf dem Bildschirm bevorzugen, dass ein Dienst nicht gestartet werden konnte, können Sie den Fehlercode mithilfe von WMI ändern.</span><span class="sxs-lookup"><span data-stu-id="e05d7-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="e05d7-291">Fehler Steuerungs Codes gelten nur für den Computer Start. Es werden keine Fehlercodes verwendet, wenn Sie einen Dienst nach dem Ausführen des Computers abbrechen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="e05d7-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="e05d7-292">Gelegentlich müssen Sie möglicherweise das Konto ändern, unter dem ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="e05d7-293">Beispielsweise können Sie einen Dienst unter einem Administrator Konto ausführen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="e05d7-294">Da dadurch ein Sicherheitsrisiko entstehen kann, können Sie den Dienst zu einem Konto mit weniger Berechtigungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="e05d7-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="e05d7-295">Möglicherweise verfügen Sie auch über Dienste, die unter einem Konto ausgeführt werden, das gelöscht werden soll, oder Sie möchten sicherstellen, dass bestimmte Dienste auf allen Servern unter bestimmten Konten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="e05d7-296">Sie können die **Änderungs** Methode der Win32- [**\_ Dienst**](win32-service.md) Klasse verwenden, um Dienste so zu konfigurieren, dass Sie unter einem angegebenen Benutzerkonto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="e05d7-297">Wenn Sie ein Konto auswählen, beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e05d7-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="e05d7-298">Das Konto, das als Dienst Konto verwendet wird, muss über die Berechtigung verfügen, sich als Dienst anzumelden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="e05d7-299">Dieses Recht kann mithilfe von Gruppenrichtlinie erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="e05d7-300">Das Konto, das als Dienst Konto verwendet wird, sollte nicht Mitglied einer lokalen Gruppe, einer Domäne oder einer Organisations Administratoren Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="e05d7-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="e05d7-301">Jede Instanz eines Dienstanbieter sollte unter einem eindeutigen Benutzerkonto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="e05d7-302">Dies bietet zusätzliche Sicherheit und ermöglicht die Überwachung einzelner Dienst Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="e05d7-303">Wenn der Dienst interaktiv ist, muss der Dienst unter dem Konto "LocalSystem" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="e05d7-304">"LocalSystem" ist erforderlich, da jeweils nur eine Fenster Station (WinSta0) sichtbar und interaktiv sein kann.</span><span class="sxs-lookup"><span data-stu-id="e05d7-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="e05d7-305">Wenn ein Dienst unter einem anderen Konto als "LocalSystem" ausgeführt wird, wird er auf der Standard Station des Dienst-0x03e7 $-Fensters ausgeführt, bei dem es sich \\ um ein unsichtbares Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="e05d7-306">Dienste, die in dieser Fenster Station ausgeführt werden, können keine Eingabe-oder Anzeige Ausgabe empfangen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="e05d7-307">Wenn Sie ein Konto einem Dienst zuweisen, benötigt der SCM das richtige Kennwort für dieses Konto, bevor die Zuweisung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="e05d7-308">Wenn Sie ein falsches Kennwort angeben, lehnt der SCM das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="e05d7-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="e05d7-309">Wenn Sie ein Dienst Konto mit dem Konto "LocalSystem", "LocalService" oder "Network Service" konfigurieren, müssen Sie kein Konto Kennwort angeben, da diese Konten keine Kenn Wörter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e05d7-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="e05d7-310">Der SCM speichert das Konto Kennwort in der Dienst Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e05d7-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="e05d7-311">Nachdem das Kennwort zugewiesen wurde, stellt der SCM jedoch nicht sicher, dass das Kennwort, das in der Dienst Datenbank gespeichert ist, und das Kennwort, das dem Benutzerkonto in zugewiesen ist, weiterhin mit der Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e05d7-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="e05d7-312">Folglich könnte eine ähnliche Situation wie die folgende auftreten:</span><span class="sxs-lookup"><span data-stu-id="e05d7-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="e05d7-313">Sie konfigurieren einen Dienst, der unter einem bestimmten Benutzerkonto ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e05d7-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="e05d7-314">Der Dienst wird mit dem aktuellen Konto Kennwort unter diesem Konto gestartet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="e05d7-315">Sie ändern das Kennwort für das Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="e05d7-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="e05d7-316">Der Dienst wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e05d7-316">The service continues to run.</span></span> <span data-ttu-id="e05d7-317">Wenn der Dienst jedoch beendet wird, können Sie ihn nicht neu starten, da der SCM weiterhin das alte, ungültige Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="e05d7-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="e05d7-318">Wenn Sie das Kennwort in Active Directory ändern, wird das in der Dienst Datenbank gespeicherte Kennwort nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="e05d7-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="e05d7-319">Wenn Sie Dienste unter regulären Benutzerkonten ausführen, müssen Sie diese Dienst Kennwörter jedes Mal aktualisieren, wenn das Kennwort des Benutzerkontos geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e05d7-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="e05d7-320">Dies kann besonders zeitaufwändig sein, wenn Sie nicht sicher sind, welche Dienste unter diesem Konto ausgeführt werden oder welche Computer über Dienste verfügen, die unter diesem Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e05d7-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="e05d7-321">Glücklicherweise können Sie WMI verwenden, um die Dienst Konten auf allen Computern zu überprüfen und ggf. das Kennwort des Dienst Kontos zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e05d7-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="e05d7-322">Der [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) -Parameter stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="e05d7-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="e05d7-323">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e05d7-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="e05d7-324">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e05d7-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="e05d7-325">Um einen Dienst von einem Netzwerkdienst in ein lokales System zu ändern, müssen die Parameter " *StartName* " und " *startpassword* " die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e05d7-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="e05d7-326">Um einen Dienst von einem lokalen Systemdienst in ein Netzwerk zu ändern, müssen die Parameter " *StartName* " und " *startpassword* " die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e05d7-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="e05d7-327">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e05d7-327">Examples</span></span>

<span data-ttu-id="e05d7-328">Das folgende VBScript ändert das Dienst Konto für Dienste von der Ausführung unter einem angegebenen Benutzerkonto in "LocalSystem".</span><span class="sxs-lookup"><span data-stu-id="e05d7-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="e05d7-329">Das folgende VBScript ändert das Dienst Konto Kennwort für alle Skripts, die unter "nettsvc" ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="e05d7-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="e05d7-330">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e05d7-330">Requirements</span></span>



| <span data-ttu-id="e05d7-331">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e05d7-331">Requirement</span></span> | <span data-ttu-id="e05d7-332">Wert</span><span class="sxs-lookup"><span data-stu-id="e05d7-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e05d7-333">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e05d7-333">Minimum supported client</span></span><br/> | <span data-ttu-id="e05d7-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e05d7-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e05d7-335">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e05d7-335">Minimum supported server</span></span><br/> | <span data-ttu-id="e05d7-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e05d7-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e05d7-337">Namespace</span><span class="sxs-lookup"><span data-stu-id="e05d7-337">Namespace</span></span><br/>                | <span data-ttu-id="e05d7-338">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e05d7-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e05d7-339">Header</span><span class="sxs-lookup"><span data-stu-id="e05d7-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="e05d7-340"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e05d7-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="e05d7-341">MOF</span><span class="sxs-lookup"><span data-stu-id="e05d7-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e05d7-342"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e05d7-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e05d7-343">DLL</span><span class="sxs-lookup"><span data-stu-id="e05d7-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e05d7-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e05d7-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e05d7-345">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e05d7-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="e05d7-346">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e05d7-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e05d7-347">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="e05d7-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="e05d7-348">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="e05d7-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

