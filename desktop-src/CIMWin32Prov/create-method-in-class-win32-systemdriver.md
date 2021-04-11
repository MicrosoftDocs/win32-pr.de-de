---
description: Erstellt einen neuen Dienst, der vom System Treiber verwaltet wird.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Create-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127764"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="44990-103">Create-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="44990-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="44990-104">Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen Dienst, der vom System Treiber verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="44990-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="44990-105">Der *Win32 \_ LoadOrderGroup* -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="44990-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="44990-106">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="44990-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="44990-107">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="44990-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="44990-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="44990-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44990-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="44990-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44990-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="44990-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="44990-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="44990-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44990-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-113">Name des Dienstanbieter, der in der **Create** -Methode installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="44990-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="44990-114">Die maximale Zeichen folgen Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="44990-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="44990-115">Die Dienst Steuerungs Verwaltung behält die Groß-/Kleinschreibung der Zeichen bei. bei Dienstnamen vergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="44990-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="44990-116">Vorwärts Schrägstriche (/) und doppelte umgekehrte Schrägstriche ( \\ ) sind ungültige Dienstnamen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="44990-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="44990-117">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-118">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="44990-118">Display name of the service.</span></span> <span data-ttu-id="44990-119">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="44990-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="44990-120">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="44990-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="44990-121">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="44990-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="44990-122">Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="44990-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="44990-123">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="44990-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="44990-124">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-125">Voll qualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="44990-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="44990-126">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="44990-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="44990-127">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-128">Typ der Dienste, die für die Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="44990-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="44990-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="44990-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="44990-130">Kernel Treiber</span><span class="sxs-lookup"><span data-stu-id="44990-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="44990-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="44990-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="44990-132">Datei System Treiber</span><span class="sxs-lookup"><span data-stu-id="44990-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="44990-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="44990-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="44990-134">Adapter</span><span class="sxs-lookup"><span data-stu-id="44990-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="44990-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="44990-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="44990-136">Erkennungs Treiber</span><span class="sxs-lookup"><span data-stu-id="44990-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="44990-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="44990-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="44990-138">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="44990-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="44990-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="44990-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="44990-140">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="44990-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="44990-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="44990-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="44990-142">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="44990-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="44990-143">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-144">Der Schweregrad des Fehlers, wenn die **Create** -Methode nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="44990-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="44990-145">Dieser Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="44990-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="44990-146">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="44990-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="44990-147">0</span><span class="sxs-lookup"><span data-stu-id="44990-147">0</span></span>
</dt> <dd>

<span data-ttu-id="44990-148">Lassen</span><span class="sxs-lookup"><span data-stu-id="44990-148">"Ignore"</span></span>

<span data-ttu-id="44990-149">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="44990-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="44990-150">1</span><span class="sxs-lookup"><span data-stu-id="44990-150">1</span></span>
</dt> <dd>

<span data-ttu-id="44990-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="44990-151">"Normal"</span></span>

<span data-ttu-id="44990-152">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="44990-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="44990-153">2</span><span class="sxs-lookup"><span data-stu-id="44990-153">2</span></span>
</dt> <dd>

<span data-ttu-id="44990-154">Starkem</span><span class="sxs-lookup"><span data-stu-id="44990-154">"Severe"</span></span>

<span data-ttu-id="44990-155">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="44990-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="44990-156">3</span><span class="sxs-lookup"><span data-stu-id="44990-156">3</span></span>
</dt> <dd>

<span data-ttu-id="44990-157">Kritisch</span><span class="sxs-lookup"><span data-stu-id="44990-157">"Critical"</span></span>

<span data-ttu-id="44990-158">Das System versucht, mit einer guten Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="44990-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="44990-159">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-160">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="44990-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="44990-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Starten**</span><span class="sxs-lookup"><span data-stu-id="44990-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="44990-162">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="44990-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="44990-163">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="44990-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="44990-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Anlage**</span><span class="sxs-lookup"><span data-stu-id="44990-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="44990-165">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="44990-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="44990-166">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="44990-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="44990-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**</span><span class="sxs-lookup"><span data-stu-id="44990-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="44990-168">Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="44990-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="44990-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**</span><span class="sxs-lookup"><span data-stu-id="44990-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="44990-170">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="44990-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="44990-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="44990-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="44990-172">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="44990-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="44990-173">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-174">**True** gibt an, dass der Dienst die Fenster auf dem Desktop erstellen oder mit Ihnen kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="44990-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="44990-175">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-176">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44990-176">Account name under which the service runs.</span></span> <span data-ttu-id="44990-177">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder "Benutzer Prinzipal Name (UPN) Format ()" aufweisen Username@DomainName .</span><span class="sxs-lookup"><span data-stu-id="44990-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="44990-178">Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44990-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="44990-179">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44990-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="44990-180">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="44990-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="44990-181">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44990-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="44990-182">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="44990-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="44990-183">Beispiel: dwdom- \\ Administrator</span><span class="sxs-lookup"><span data-stu-id="44990-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="44990-184">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-185">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44990-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="44990-186">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="44990-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="44990-187">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="44990-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="44990-188">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-189">Der dem neuen Dienst zugeordnete Gruppenname.</span><span class="sxs-lookup"><span data-stu-id="44990-189">Group name associated with the new service.</span></span> <span data-ttu-id="44990-190">Lade Reihen folgen Gruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="44990-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="44990-191">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge verweist, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="44990-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="44990-192">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="44990-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="44990-193">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="44990-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="44990-194">Die Registrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="44990-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="44990-195">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="44990-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="44990-196">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-197">Array von Gruppen für die Auslastungs Anordnung, die vor diesem Dienst gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="44990-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="44990-198">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="44990-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="44990-199">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="44990-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="44990-200">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="44990-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="44990-201">Gruppennamen muss der **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um ihn von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="44990-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="44990-202">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="44990-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="44990-203">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44990-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44990-204">Ein Array, das die Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="44990-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="44990-205">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="44990-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="44990-206">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="44990-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="44990-207">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="44990-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="44990-208">Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44990-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44990-209">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44990-209">Return value</span></span>

<span data-ttu-id="44990-210">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich erstellt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="44990-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="44990-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44990-211">Requirements</span></span>



| <span data-ttu-id="44990-212">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44990-212">Requirement</span></span> | <span data-ttu-id="44990-213">Wert</span><span class="sxs-lookup"><span data-stu-id="44990-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44990-214">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44990-214">Minimum supported client</span></span><br/> | <span data-ttu-id="44990-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44990-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44990-216">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44990-216">Minimum supported server</span></span><br/> | <span data-ttu-id="44990-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44990-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44990-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="44990-218">Namespace</span></span><br/>                | <span data-ttu-id="44990-219">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44990-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44990-220">MOF</span><span class="sxs-lookup"><span data-stu-id="44990-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44990-221"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="44990-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44990-222">DLL</span><span class="sxs-lookup"><span data-stu-id="44990-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44990-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44990-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44990-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44990-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="44990-225">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44990-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="44990-226">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="44990-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

