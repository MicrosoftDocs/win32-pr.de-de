---
description: Ändert einen Win32 \_ systemdriver-Dienst.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Change-Methode der Win32_SystemDriver-Klasse (mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483563"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="77e0a-103">Change-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="77e0a-103">Change method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="77e0a-104">Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert einen [**Win32 \_ systemdriver**](win32-systemdriver.md) -Dienst.</span><span class="sxs-lookup"><span data-stu-id="77e0a-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span> <span data-ttu-id="77e0a-105">Der [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="77e0a-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="77e0a-106">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="77e0a-106">The services must be initiated in the order specified by the Load Order Group as the services are dependent on each other.</span></span> <span data-ttu-id="77e0a-107">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="77e0a-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="77e0a-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="77e0a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="77e0a-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="77e0a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="77e0a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="77e0a-110">Syntax</span></span>


```mof
uint32 Change(
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



## <a name="parameters"></a><span data-ttu-id="77e0a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="77e0a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e0a-112">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-113">Der Anzeigename des Diensts</span><span class="sxs-lookup"><span data-stu-id="77e0a-113">The display name of the service.</span></span> <span data-ttu-id="77e0a-114">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="77e0a-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="77e0a-115">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="77e0a-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="77e0a-116">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="77e0a-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="77e0a-117">Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="77e0a-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="77e0a-118">Beispiel: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="77e0a-118">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-119">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-120">Der voll qualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="77e0a-120">The fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="77e0a-121">Beispiel: *\\ systemroot \\ system32 \\ Drivers \\afd.sys*</span><span class="sxs-lookup"><span data-stu-id="77e0a-121">Example: *\\SystemRoot\\System32\\drivers\\afd.sys*</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-122">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-123">Typ der Dienste, die für die Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="77e0a-123">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="77e0a-124">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="77e0a-124">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-125">Kernel Treiber</span><span class="sxs-lookup"><span data-stu-id="77e0a-125">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="77e0a-126">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-127">Datei System Treiber</span><span class="sxs-lookup"><span data-stu-id="77e0a-127">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="77e0a-128">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-129">Adapter</span><span class="sxs-lookup"><span data-stu-id="77e0a-129">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-130">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="77e0a-130">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-131">Erkennungs Treiber</span><span class="sxs-lookup"><span data-stu-id="77e0a-131">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-132">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="77e0a-132">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-133">Eigener Prozess</span><span class="sxs-lookup"><span data-stu-id="77e0a-133">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-134">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="77e0a-134">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-135">Freigabeprozess</span><span class="sxs-lookup"><span data-stu-id="77e0a-135">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-136">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="77e0a-136">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-137">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="77e0a-137">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="77e0a-138">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-139">Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="77e0a-139">The severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="77e0a-140">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="77e0a-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="77e0a-141">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="77e0a-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="77e0a-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** (0)</span><span class="sxs-lookup"><span data-stu-id="77e0a-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-143">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="77e0a-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="77e0a-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="77e0a-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-145">Normal.</span><span class="sxs-lookup"><span data-stu-id="77e0a-145">Normal.</span></span> <span data-ttu-id="77e0a-146">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="77e0a-146">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="77e0a-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)</span><span class="sxs-lookup"><span data-stu-id="77e0a-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-148">Das System wird mit der letzten guten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="77e0a-148">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="77e0a-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="77e0a-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-150">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="77e0a-150">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="77e0a-151">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-151">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-152">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="77e0a-152">The start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="77e0a-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start**</span><span class="sxs-lookup"><span data-stu-id="77e0a-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-154">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="77e0a-154">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="77e0a-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start**</span><span class="sxs-lookup"><span data-stu-id="77e0a-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-156">Gerätetreiber, der vom Betriebssystem Lader gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="77e0a-156">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="77e0a-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span><span class="sxs-lookup"><span data-stu-id="77e0a-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-158">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="77e0a-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="77e0a-159">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="77e0a-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="77e0a-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatisch starten**</span><span class="sxs-lookup"><span data-stu-id="77e0a-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start**</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-161">Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="77e0a-161">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="77e0a-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start**</span><span class="sxs-lookup"><span data-stu-id="77e0a-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start**</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-163">Dienst, der vom Dienststeuerungs-Manager gestartet wird, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="77e0a-163">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="77e0a-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="77e0a-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="77e0a-165">Dienst, der nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="77e0a-165">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="77e0a-166">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-167">Ein-Wert, der, wenn der Wert **true** ist, den Windows-Dienst auf dem Desktop erstellen oder mit diesem kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="77e0a-167">A value that, if **True**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-168">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-169">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77e0a-169">The account name the service runs under.</span></span> <span data-ttu-id="77e0a-170">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name Benutzername" oder "" aufweisen \\ . \\ User.</span><span class="sxs-lookup"><span data-stu-id="77e0a-170">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="77e0a-171">Bei der Ausführung wird der Dienst Prozess mit einer dieser beiden Formulare protokolliert.</span><span class="sxs-lookup"><span data-stu-id="77e0a-171">When it runs, the service process is logged using one of these two forms.</span></span> <span data-ttu-id="77e0a-172">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77e0a-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="77e0a-173">Wenn eine leere Zeichenfolge angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="77e0a-173">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="77e0a-174">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen, z \\ . b. Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77e0a-174">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns), which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="77e0a-175">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, den das e/a-System basierend auf dem Dienstnamen erstellt, z. b. dwdom \\ Admin.</span><span class="sxs-lookup"><span data-stu-id="77e0a-175">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="77e0a-176">Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..</span><span class="sxs-lookup"><span data-stu-id="77e0a-176">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-177">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-178">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77e0a-178">The password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="77e0a-179">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="77e0a-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="77e0a-180">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="77e0a-180">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="77e0a-181">Wenn ein Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk auf ein lokales System geändert wird, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="77e0a-181">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="77e0a-182">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-182">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-183">Der Gruppenname, dem er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="77e0a-183">The group name that it is associated with.</span></span> <span data-ttu-id="77e0a-184">Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="77e0a-184">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="77e0a-185">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="77e0a-185">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="77e0a-186">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="77e0a-186">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="77e0a-187">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="77e0a-187">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="77e0a-188">Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="77e0a-188">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="77e0a-189">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="77e0a-189">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-190">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-190">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-191">Die Liste der Gruppen mit Lade Reihen, die vor dem Start dieses Dienstanbieter gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="77e0a-191">The list of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="77e0a-192">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="77e0a-192">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="77e0a-193">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="77e0a-193">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="77e0a-194">Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um Sie von Dienstnamen zu unterscheiden, weil Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="77e0a-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the WinSvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="77e0a-195">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="77e0a-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="77e0a-196">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77e0a-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e0a-197">Die Liste, die die Namen der Dienste enthält, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="77e0a-197">The list that contains the names of the services that must start before this service starts.</span></span> <span data-ttu-id="77e0a-198">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="77e0a-198">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="77e0a-199">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="77e0a-199">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="77e0a-200">Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77e0a-200">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e0a-201">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77e0a-201">Return value</span></span>

<span data-ttu-id="77e0a-202">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich geändert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="77e0a-202">Returns a value of zero (0) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="77e0a-203">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="77e0a-203">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-204">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="77e0a-204">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-205">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="77e0a-205">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-206">**Abhängige Dienste werden ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="77e0a-206">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-207">**Ungültige Dienst Kontrolle** (4).</span><span class="sxs-lookup"><span data-stu-id="77e0a-207">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-208">Der **Dienst kann die Steuerung nicht akzeptieren** (5).</span><span class="sxs-lookup"><span data-stu-id="77e0a-208">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-209">Der **Dienst ist nicht aktiv** (6).</span><span class="sxs-lookup"><span data-stu-id="77e0a-209">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-210">**Timeout für Dienst Anforderungen** (7)</span><span class="sxs-lookup"><span data-stu-id="77e0a-210">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-211">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="77e0a-211">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-212">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="77e0a-212">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-213">Der **Dienst wird bereits ausgeführt** (10).</span><span class="sxs-lookup"><span data-stu-id="77e0a-213">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-214">**Dienst Datenbank gesperrt** (11)</span><span class="sxs-lookup"><span data-stu-id="77e0a-214">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-215">**Dienst Abhängigkeit gelöscht** (12)</span><span class="sxs-lookup"><span data-stu-id="77e0a-215">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-216">**Dienst Abhängigkeitsfehler** (13)</span><span class="sxs-lookup"><span data-stu-id="77e0a-216">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-217">**Dienst deaktiviert** (14)</span><span class="sxs-lookup"><span data-stu-id="77e0a-217">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-218">Fehler bei der **Dienst Anmeldung** (15).</span><span class="sxs-lookup"><span data-stu-id="77e0a-218">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-219">Der **Dienst wurde zum Löschen markiert** (16).</span><span class="sxs-lookup"><span data-stu-id="77e0a-219">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-220">**Dienst ohne Thread** (17)</span><span class="sxs-lookup"><span data-stu-id="77e0a-220">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-221">**Status zirkuläre Abhängigkeit** (18)</span><span class="sxs-lookup"><span data-stu-id="77e0a-221">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-222">**Doppelter Name des Status** (19)</span><span class="sxs-lookup"><span data-stu-id="77e0a-222">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-223">**Ungültiger Name** (20).</span><span class="sxs-lookup"><span data-stu-id="77e0a-223">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-224">**Ungültiger Parameter** (21).</span><span class="sxs-lookup"><span data-stu-id="77e0a-224">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-225">**Ungültiges Dienst Konto** (22).</span><span class="sxs-lookup"><span data-stu-id="77e0a-225">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-226">**Status Dienst vorhanden** (23)</span><span class="sxs-lookup"><span data-stu-id="77e0a-226">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-227">Der **Dienst wurde bereits angeh** alten (24).</span><span class="sxs-lookup"><span data-stu-id="77e0a-227">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="77e0a-228">**Sonstige** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="77e0a-228">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="77e0a-229">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77e0a-229">Remarks</span></span>

<span data-ttu-id="77e0a-230">Um einen Dienst von einem Netzwerkdienst in das lokale System zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":</span><span class="sxs-lookup"><span data-stu-id="77e0a-230">To change a service from a network service to the local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="77e0a-231">Um einen Dienst von einem lokalen Systemdienst in einen Netzwerkdienst zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":</span><span class="sxs-lookup"><span data-stu-id="77e0a-231">To change a service from a local system service to network service, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="77e0a-232">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77e0a-232">Requirements</span></span>



| <span data-ttu-id="77e0a-233">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77e0a-233">Requirement</span></span> | <span data-ttu-id="77e0a-234">Wert</span><span class="sxs-lookup"><span data-stu-id="77e0a-234">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77e0a-235">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77e0a-235">Minimum supported client</span></span><br/> | <span data-ttu-id="77e0a-236">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77e0a-236">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77e0a-237">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77e0a-237">Minimum supported server</span></span><br/> | <span data-ttu-id="77e0a-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77e0a-238">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77e0a-239">Namespace</span><span class="sxs-lookup"><span data-stu-id="77e0a-239">Namespace</span></span><br/>                | <span data-ttu-id="77e0a-240">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="77e0a-240">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77e0a-241">Header</span><span class="sxs-lookup"><span data-stu-id="77e0a-241">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e0a-242"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e0a-242"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="77e0a-243">MOF</span><span class="sxs-lookup"><span data-stu-id="77e0a-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77e0a-244"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="77e0a-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77e0a-245">DLL</span><span class="sxs-lookup"><span data-stu-id="77e0a-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e0a-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e0a-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e0a-247">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77e0a-247">See also</span></span>

<dl> <dt>

<span data-ttu-id="77e0a-248">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77e0a-248">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="77e0a-249">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="77e0a-249">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

