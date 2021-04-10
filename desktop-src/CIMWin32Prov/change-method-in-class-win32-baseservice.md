---
description: Ändert ein Dienst Objekt, das von Win32 \_ baseservice abgeleitet ist.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Change-Methode der Win32_BaseService-Klasse (mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127228"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="5fc34-103">Change-Methode der Win32 \_ baseservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="5fc34-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="5fc34-104">Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert ein Dienst Objekt, das von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="5fc34-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="5fc34-105">Der [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) -Parameter stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="5fc34-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="5fc34-106">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5fc34-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="5fc34-107">Diese abhängigen Dienste erfordern, dass Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5fc34-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="5fc34-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fc34-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5fc34-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5fc34-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc34-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fc34-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5fc34-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fc34-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc34-112">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-113">Der Anzeige Name für einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="5fc34-113">The display name for a service.</span></span> <span data-ttu-id="5fc34-114">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5fc34-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="5fc34-115">Der Name wird im Dienststeuerungs-Manager beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5fc34-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="5fc34-116">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="5fc34-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="5fc34-117">Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5fc34-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="5fc34-118">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="5fc34-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-119">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-120">Der voll qualifizierte Pfad zur ausführbaren Datei, die einen Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="5fc34-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="5fc34-121">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="5fc34-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-122">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-123">Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="5fc34-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="5fc34-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Treiber** (1)</span><span class="sxs-lookup"><span data-stu-id="5fc34-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="5fc34-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Datei System Treiber** (2)</span><span class="sxs-lookup"><span data-stu-id="5fc34-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="5fc34-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span><span class="sxs-lookup"><span data-stu-id="5fc34-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="5fc34-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Erkennungs Treiber** (8)</span><span class="sxs-lookup"><span data-stu-id="5fc34-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="5fc34-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Eigener Prozess** (16)</span><span class="sxs-lookup"><span data-stu-id="5fc34-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="5fc34-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Freigabeprozess** (32)</span><span class="sxs-lookup"><span data-stu-id="5fc34-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc34-130">(256)</span><span class="sxs-lookup"><span data-stu-id="5fc34-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-131">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="5fc34-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5fc34-132">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-133">Schweregrad eines Fehlers, wenn dieser Dienst nicht während des Starts gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5fc34-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="5fc34-134">Der Wert gibt die Aktion an, die das Start Programm durchführt, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="5fc34-135">Das System protokolliert alle Fehler.</span><span class="sxs-lookup"><span data-stu-id="5fc34-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="5fc34-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** (0)</span><span class="sxs-lookup"><span data-stu-id="5fc34-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-137">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="5fc34-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="5fc34-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-139">Normal.</span><span class="sxs-lookup"><span data-stu-id="5fc34-139">Normal.</span></span> <span data-ttu-id="5fc34-140">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="5fc34-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)</span><span class="sxs-lookup"><span data-stu-id="5fc34-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-142">Das System wird mit der letzten guten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5fc34-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5fc34-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="5fc34-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-144">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="5fc34-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5fc34-145">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-146">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="5fc34-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="5fc34-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="5fc34-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-148">Gerätetreiber, der vom Betriebssystem Lader gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5fc34-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="5fc34-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span><span class="sxs-lookup"><span data-stu-id="5fc34-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-150">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="5fc34-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="5fc34-151">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="5fc34-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="5fc34-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="5fc34-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-153">Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5fc34-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="5fc34-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="5fc34-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-155">Dienst, der vom Dienststeuerungs-Manager gestartet wird, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-baseservice.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="5fc34-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5fc34-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="5fc34-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="5fc34-157">Dienst, der nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fc34-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5fc34-158">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-159">**True** gibt an, dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="5fc34-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-160">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-161">Der Kontoname, unter dem der Dienst ausgeführt wird, der vom Diensttyp abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="5fc34-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="5fc34-162">Der Kontoname kann in der Form Domänen Name \\ Benutzername oder lauten \\ . User.</span><span class="sxs-lookup"><span data-stu-id="5fc34-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="5fc34-163">Bei der Ausführung wird der Dienst Prozess mit einer der beiden vorherigen Formen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="5fc34-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="5fc34-164">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="5fc34-165">Wenn eine leere Zeichenfolge angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="5fc34-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="5fc34-166">Für Treiber auf Kernel-oder Systemebene enthält *StartName* den Treiber Objektnamen, z \\ . b. Dateisystem- \\ rdr oder \\ Treiber- \\ xns, die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="5fc34-167">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, den das e/a-System basierend auf dem Dienstnamen erstellt, z. b. dwdom \\ Admin.</span><span class="sxs-lookup"><span data-stu-id="5fc34-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="5fc34-168">Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..</span><span class="sxs-lookup"><span data-stu-id="5fc34-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-169">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-170">Kennwort für den Kontonamen, den der *StartName* -Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="5fc34-171">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="5fc34-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="5fc34-172">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="5fc34-173">Wenn Sie einen Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk in ein lokales System ändern, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="5fc34-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="5fc34-174">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-175">Der Gruppenname, dem er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5fc34-175">Group name that it is associated with.</span></span> <span data-ttu-id="5fc34-176">Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der die Dienste in ein Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="5fc34-177">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5fc34-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="5fc34-178">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="5fc34-179">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="5fc34-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="5fc34-180">Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen, die sich unter **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder** befinden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-181">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-182">Liste der Lade Gruppen, die vor dem Start dieses Dienstanbieter gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5fc34-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="5fc34-183">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="5fc34-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5fc34-184">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="5fc34-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="5fc34-185">Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um Sie von Dienstnamen zu unterscheiden, weil Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="5fc34-186">Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="5fc34-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-187">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fc34-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-188">Liste mit den Namen der Dienste, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5fc34-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="5fc34-189">Das Array ist doppelt **null**-terminiert.</span><span class="sxs-lookup"><span data-stu-id="5fc34-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5fc34-190">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="5fc34-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="5fc34-191">Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc34-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc34-192">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fc34-192">Return value</span></span>

<span data-ttu-id="5fc34-193">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5fc34-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5fc34-194">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="5fc34-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-195">0</span><span class="sxs-lookup"><span data-stu-id="5fc34-195">0</span></span>

<span data-ttu-id="5fc34-196">Die Anforderung wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5fc34-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-197">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="5fc34-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-198">1</span><span class="sxs-lookup"><span data-stu-id="5fc34-198">1</span></span>

<span data-ttu-id="5fc34-199">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-200">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="5fc34-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-201">2</span><span class="sxs-lookup"><span data-stu-id="5fc34-201">2</span></span>

<span data-ttu-id="5fc34-202">Der Benutzer verfügt nicht über die erforderlichen Zugriffsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="5fc34-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-203">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="5fc34-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-204">3</span><span class="sxs-lookup"><span data-stu-id="5fc34-204">3</span></span>

<span data-ttu-id="5fc34-205">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5fc34-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-206">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-207">4</span><span class="sxs-lookup"><span data-stu-id="5fc34-207">4</span></span>

<span data-ttu-id="5fc34-208">Der angeforderte Steuerungs Code ist ungültig oder für den Dienst nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5fc34-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-209">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-210">5</span><span class="sxs-lookup"><span data-stu-id="5fc34-210">5</span></span>

<span data-ttu-id="5fc34-211">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, da die [**State**](win32-baseservice.md) -Eigenschaft im [**Win32- \_ baseservice**](win32-baseservice.md) -Objekt gleich 0, 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="5fc34-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-212">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="5fc34-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-213">6</span><span class="sxs-lookup"><span data-stu-id="5fc34-213">6</span></span>

<span data-ttu-id="5fc34-214">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="5fc34-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-215">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="5fc34-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-216">7</span><span class="sxs-lookup"><span data-stu-id="5fc34-216">7</span></span>

<span data-ttu-id="5fc34-217">Der Dienst antwortet nicht schnell auf die Start Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5fc34-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-218">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-219">8</span><span class="sxs-lookup"><span data-stu-id="5fc34-219">8</span></span>

<span data-ttu-id="5fc34-220">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="5fc34-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-221">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="5fc34-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-222">9</span><span class="sxs-lookup"><span data-stu-id="5fc34-222">9</span></span>

<span data-ttu-id="5fc34-223">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-224">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-225">10</span><span class="sxs-lookup"><span data-stu-id="5fc34-225">10</span></span>

<span data-ttu-id="5fc34-226">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-227">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="5fc34-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-228">11</span><span class="sxs-lookup"><span data-stu-id="5fc34-228">11</span></span>

<span data-ttu-id="5fc34-229">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-230">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="5fc34-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-231">12</span><span class="sxs-lookup"><span data-stu-id="5fc34-231">12</span></span>

<span data-ttu-id="5fc34-232">Eine Abhängigkeit, von der dieser Dienst abhängig ist, wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-233">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="5fc34-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-234">13</span><span class="sxs-lookup"><span data-stu-id="5fc34-234">13</span></span>

<span data-ttu-id="5fc34-235">Der Dienst findet den von einem abhängigen Dienst benötigten Dienst nicht.</span><span class="sxs-lookup"><span data-stu-id="5fc34-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-236">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="5fc34-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-237">14</span><span class="sxs-lookup"><span data-stu-id="5fc34-237">14</span></span>

<span data-ttu-id="5fc34-238">Der Dienst ist im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5fc34-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-239">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="5fc34-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-240">15</span><span class="sxs-lookup"><span data-stu-id="5fc34-240">15</span></span>

<span data-ttu-id="5fc34-241">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-242">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-243">16</span><span class="sxs-lookup"><span data-stu-id="5fc34-243">16</span></span>

<span data-ttu-id="5fc34-244">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-245">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="5fc34-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-246">17</span><span class="sxs-lookup"><span data-stu-id="5fc34-246">17</span></span>

<span data-ttu-id="5fc34-247">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="5fc34-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-248">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="5fc34-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-249">18</span><span class="sxs-lookup"><span data-stu-id="5fc34-249">18</span></span>

<span data-ttu-id="5fc34-250">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="5fc34-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-251">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="5fc34-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-252">19</span><span class="sxs-lookup"><span data-stu-id="5fc34-252">19</span></span>

<span data-ttu-id="5fc34-253">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-254">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="5fc34-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-255">20</span><span class="sxs-lookup"><span data-stu-id="5fc34-255">20</span></span>

<span data-ttu-id="5fc34-256">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5fc34-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-257">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-258">21</span><span class="sxs-lookup"><span data-stu-id="5fc34-258">21</span></span>

<span data-ttu-id="5fc34-259">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5fc34-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-260">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-261">22</span><span class="sxs-lookup"><span data-stu-id="5fc34-261">22</span></span>

<span data-ttu-id="5fc34-262">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="5fc34-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-263">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="5fc34-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-264">23</span><span class="sxs-lookup"><span data-stu-id="5fc34-264">23</span></span>

<span data-ttu-id="5fc34-265">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5fc34-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-266">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="5fc34-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-267">24</span><span class="sxs-lookup"><span data-stu-id="5fc34-267">24</span></span>

<span data-ttu-id="5fc34-268">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="5fc34-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="5fc34-269">**Andere**</span><span class="sxs-lookup"><span data-stu-id="5fc34-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5fc34-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="5fc34-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fc34-271">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fc34-271">Remarks</span></span>

<span data-ttu-id="5fc34-272">Um einen Dienst von einem Netzwerk auf ein lokales System zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":</span><span class="sxs-lookup"><span data-stu-id="5fc34-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="5fc34-273">Um einen Dienst von einem lokalen System in ein Netzwerk zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":</span><span class="sxs-lookup"><span data-stu-id="5fc34-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="5fc34-274">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fc34-274">Requirements</span></span>



| <span data-ttu-id="5fc34-275">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fc34-275">Requirement</span></span> | <span data-ttu-id="5fc34-276">Wert</span><span class="sxs-lookup"><span data-stu-id="5fc34-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc34-277">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fc34-277">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc34-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fc34-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5fc34-279">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fc34-279">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc34-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fc34-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5fc34-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fc34-281">Namespace</span></span><br/>                | <span data-ttu-id="5fc34-282">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5fc34-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5fc34-283">Header</span><span class="sxs-lookup"><span data-stu-id="5fc34-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc34-284"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc34-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="5fc34-285">MOF</span><span class="sxs-lookup"><span data-stu-id="5fc34-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fc34-286"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5fc34-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fc34-287">DLL</span><span class="sxs-lookup"><span data-stu-id="5fc34-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fc34-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fc34-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc34-289">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fc34-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fc34-290">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5fc34-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5fc34-291">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="5fc34-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

