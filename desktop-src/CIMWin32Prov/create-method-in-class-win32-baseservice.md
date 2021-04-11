---
description: Erstellt einen neuen Dienst.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Create-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126650"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="d5d66-103">Create-Methode der Win32 \_ baseservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d5d66-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="d5d66-104">Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen Dienst.</span><span class="sxs-lookup"><span data-stu-id="d5d66-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="d5d66-105">Der *LoadOrderGroup* -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="d5d66-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="d5d66-106">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d5d66-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="d5d66-107">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d5d66-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="d5d66-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5d66-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5d66-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d66-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5d66-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d5d66-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5d66-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d66-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-113">Name des Dienstanbieter, der in der **Create** -Methode installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5d66-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="d5d66-114">Die maximale Zeichen folgen Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="d5d66-115">Die Dienst Steuerungs Verwaltung behält die Groß-/Kleinschreibung der Zeichen bei. bei Dienstnamen vergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="d5d66-116">Vorwärts Schrägstriche (/) und doppelte umgekehrte Schrägstriche ( \\ ) sind ungültige Dienstnamen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-117">*Display Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-118">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d5d66-118">Display name of the service.</span></span> <span data-ttu-id="d5d66-119">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="d5d66-120">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d5d66-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="d5d66-121">Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="d5d66-122">Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d5d66-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="d5d66-123">Beispiel: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="d5d66-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-124">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-125">Voll qualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5d66-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="d5d66-126">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="d5d66-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-127">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-128">Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="d5d66-129">Der Wert ist eine Bitmap.</span><span class="sxs-lookup"><span data-stu-id="d5d66-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="d5d66-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Treiber** (1)</span><span class="sxs-lookup"><span data-stu-id="d5d66-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="d5d66-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Datei System Treiber** (2)</span><span class="sxs-lookup"><span data-stu-id="d5d66-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="d5d66-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span><span class="sxs-lookup"><span data-stu-id="d5d66-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="d5d66-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Erkennungs Treiber** (8)</span><span class="sxs-lookup"><span data-stu-id="d5d66-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="d5d66-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Eigener Prozess** (16)</span><span class="sxs-lookup"><span data-stu-id="d5d66-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="d5d66-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Freigabeprozess** (32)</span><span class="sxs-lookup"><span data-stu-id="d5d66-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="d5d66-136">256</span><span class="sxs-lookup"><span data-stu-id="d5d66-136">256</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-137">Interaktiver Prozess</span><span class="sxs-lookup"><span data-stu-id="d5d66-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d5d66-138">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-139">Der Schweregrad des Fehlers, wenn die **Create** -Methode nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d5d66-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="d5d66-140">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="d5d66-141">Alle Fehler werden vom System protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d5d66-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="d5d66-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** (0)</span><span class="sxs-lookup"><span data-stu-id="d5d66-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-143">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="d5d66-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="d5d66-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-145">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="d5d66-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)</span><span class="sxs-lookup"><span data-stu-id="d5d66-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-147">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d5d66-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="d5d66-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-149">Das System versucht, mit einer guten Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d5d66-150">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-151">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d5d66-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="d5d66-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="d5d66-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-153">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="d5d66-154">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="d5d66-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="d5d66-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span><span class="sxs-lookup"><span data-stu-id="d5d66-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-156">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="d5d66-157">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="d5d66-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="d5d66-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="d5d66-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-159">Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="d5d66-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="d5d66-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-161">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="d5d66-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d5d66-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="d5d66-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="d5d66-163">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d5d66-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d5d66-164">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-165">**True** gibt an, dass der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="d5d66-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-166">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-167">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d66-167">Account name under which the service runs.</span></span> <span data-ttu-id="d5d66-168">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="d5d66-169">Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d66-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="d5d66-170">Wenn das Konto zur integrierten Domäne gehört, ". \\ Username "kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="d5d66-171">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="d5d66-172">Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="d5d66-173">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5d66-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="d5d66-174">Beispiel: dwdom- \\ Administrator.</span><span class="sxs-lookup"><span data-stu-id="d5d66-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-175">*Startpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-176">Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d5d66-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="d5d66-177">Geben Sie **null** an, wenn Sie das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="d5d66-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="d5d66-178">Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-179">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-180">Der dem neuen Dienst zugeordnete Gruppenname.</span><span class="sxs-lookup"><span data-stu-id="d5d66-180">Group name associated with the new service.</span></span> <span data-ttu-id="d5d66-181">Lade Auftrags Gruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="d5d66-182">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge verweist, gehört der Dienst nicht zu einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d5d66-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="d5d66-183">Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="d5d66-184">Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="d5d66-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="d5d66-185">Die Registrierung enthält eine Liste der Lade Auftrags Gruppen unter:</span><span class="sxs-lookup"><span data-stu-id="d5d66-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="d5d66-186">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**</span><span class="sxs-lookup"><span data-stu-id="d5d66-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-187">*Loadordergroupabhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-188">Array von Gruppen für die Auslastungs Anordnung, die vor diesem Dienst gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="d5d66-189">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d5d66-190">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="d5d66-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d5d66-191">Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d5d66-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d5d66-192">Gruppennamen muss der SC- \_ Gruppen \_ Bezeichner (definiert in der Datei "winsvc. h") vorangestellt werden, um ihn von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="d5d66-193">Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.</span><span class="sxs-lookup"><span data-stu-id="d5d66-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-194">*Service Abhängigkeiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5d66-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-195">Ein Array, das Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="d5d66-196">Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d5d66-197">In Visual Basic oder Skript können Sie ein VBArray übergeben.</span><span class="sxs-lookup"><span data-stu-id="d5d66-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d5d66-198">Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d5d66-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d5d66-199">Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d66-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d66-200">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5d66-200">Return value</span></span>

<span data-ttu-id="d5d66-201">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d5d66-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5d66-202">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="d5d66-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-203">0</span><span class="sxs-lookup"><span data-stu-id="d5d66-203">0</span></span>

<span data-ttu-id="d5d66-204">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d5d66-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-205">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="d5d66-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-206">1</span><span class="sxs-lookup"><span data-stu-id="d5d66-206">1</span></span>

<span data-ttu-id="d5d66-207">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-208">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="d5d66-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-209">2</span><span class="sxs-lookup"><span data-stu-id="d5d66-209">2</span></span>

<span data-ttu-id="d5d66-210">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="d5d66-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-211">**Abhängige Dienste werden ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="d5d66-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-212">3</span><span class="sxs-lookup"><span data-stu-id="d5d66-212">3</span></span>

<span data-ttu-id="d5d66-213">Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d5d66-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-214">**Ungültige Dienst Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-215">4</span><span class="sxs-lookup"><span data-stu-id="d5d66-215">4</span></span>

<span data-ttu-id="d5d66-216">Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="d5d66-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-217">**Der Dienst kann keine Steuerung akzeptieren.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-218">5</span><span class="sxs-lookup"><span data-stu-id="d5d66-218">5</span></span>

<span data-ttu-id="d5d66-219">Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.</span><span class="sxs-lookup"><span data-stu-id="d5d66-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-220">**Dienst nicht aktiv**</span><span class="sxs-lookup"><span data-stu-id="d5d66-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-221">6</span><span class="sxs-lookup"><span data-stu-id="d5d66-221">6</span></span>

<span data-ttu-id="d5d66-222">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d5d66-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-223">**Service Request-Timeout**</span><span class="sxs-lookup"><span data-stu-id="d5d66-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-224">7</span><span class="sxs-lookup"><span data-stu-id="d5d66-224">7</span></span>

<span data-ttu-id="d5d66-225">Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.</span><span class="sxs-lookup"><span data-stu-id="d5d66-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-226">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-227">8</span><span class="sxs-lookup"><span data-stu-id="d5d66-227">8</span></span>

<span data-ttu-id="d5d66-228">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="d5d66-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-229">**Pfad nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="d5d66-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-230">9</span><span class="sxs-lookup"><span data-stu-id="d5d66-230">9</span></span>

<span data-ttu-id="d5d66-231">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-232">**Dienst wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-233">10</span><span class="sxs-lookup"><span data-stu-id="d5d66-233">10</span></span>

<span data-ttu-id="d5d66-234">Der Dienst wird schon ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-235">**Dienst Datenbank gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d5d66-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-236">11</span><span class="sxs-lookup"><span data-stu-id="d5d66-236">11</span></span>

<span data-ttu-id="d5d66-237">Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-238">**Dienst Abhängigkeit gelöscht**</span><span class="sxs-lookup"><span data-stu-id="d5d66-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-239">12</span><span class="sxs-lookup"><span data-stu-id="d5d66-239">12</span></span>

<span data-ttu-id="d5d66-240">Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-241">**Dienst Abhängigkeitsfehler**</span><span class="sxs-lookup"><span data-stu-id="d5d66-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-242">13</span><span class="sxs-lookup"><span data-stu-id="d5d66-242">13</span></span>

<span data-ttu-id="d5d66-243">Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d66-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-244">**Dienst deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d5d66-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-245">14</span><span class="sxs-lookup"><span data-stu-id="d5d66-245">14</span></span>

<span data-ttu-id="d5d66-246">Der Dienst wurde vom System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5d66-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-247">**Fehler bei der Dienst Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="d5d66-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-248">15</span><span class="sxs-lookup"><span data-stu-id="d5d66-248">15</span></span>

<span data-ttu-id="d5d66-249">Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-250">**Der Dienst wurde zum Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-251">16</span><span class="sxs-lookup"><span data-stu-id="d5d66-251">16</span></span>

<span data-ttu-id="d5d66-252">Dieser Dienst wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-253">**Dienst ohne Thread**</span><span class="sxs-lookup"><span data-stu-id="d5d66-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-254">17</span><span class="sxs-lookup"><span data-stu-id="d5d66-254">17</span></span>

<span data-ttu-id="d5d66-255">Es gibt keinen Ausführungsthread für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="d5d66-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-256">**Status zirkuläre Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="d5d66-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-257">18</span><span class="sxs-lookup"><span data-stu-id="d5d66-257">18</span></span>

<span data-ttu-id="d5d66-258">Es gibt Ringabhängigkeiten beim Starten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="d5d66-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-259">**Doppelter Name des Status**</span><span class="sxs-lookup"><span data-stu-id="d5d66-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-260">19</span><span class="sxs-lookup"><span data-stu-id="d5d66-260">19</span></span>

<span data-ttu-id="d5d66-261">Es wird ein Dienst unter dem gleichen Namen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-262">**Ungültiger Name**</span><span class="sxs-lookup"><span data-stu-id="d5d66-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-263">20</span><span class="sxs-lookup"><span data-stu-id="d5d66-263">20</span></span>

<span data-ttu-id="d5d66-264">Der Name des diensdienstanbieter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5d66-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-265">**Ungültiger Parameter.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-266">21</span><span class="sxs-lookup"><span data-stu-id="d5d66-266">21</span></span>

<span data-ttu-id="d5d66-267">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d5d66-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-268">**Ungültiges Dienst Konto.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-269">22</span><span class="sxs-lookup"><span data-stu-id="d5d66-269">22</span></span>

<span data-ttu-id="d5d66-270">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d5d66-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-271">**Status Dienst vorhanden**</span><span class="sxs-lookup"><span data-stu-id="d5d66-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-272">23</span><span class="sxs-lookup"><span data-stu-id="d5d66-272">23</span></span>

<span data-ttu-id="d5d66-273">Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d5d66-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-274">**Der Dienst wurde bereits angehalten.**</span><span class="sxs-lookup"><span data-stu-id="d5d66-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-275">24</span><span class="sxs-lookup"><span data-stu-id="d5d66-275">24</span></span>

<span data-ttu-id="d5d66-276">Der Dienst ist im System derzeitig angehalten.</span><span class="sxs-lookup"><span data-stu-id="d5d66-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d66-277">**Andere**</span><span class="sxs-lookup"><span data-stu-id="d5d66-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d5d66-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="d5d66-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d66-279">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5d66-279">Requirements</span></span>



| <span data-ttu-id="d5d66-280">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5d66-280">Requirement</span></span> | <span data-ttu-id="d5d66-281">Wert</span><span class="sxs-lookup"><span data-stu-id="d5d66-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d66-282">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5d66-282">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d66-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5d66-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5d66-284">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5d66-284">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d66-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5d66-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5d66-286">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5d66-286">Namespace</span></span><br/>                | <span data-ttu-id="d5d66-287">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d5d66-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5d66-288">MOF</span><span class="sxs-lookup"><span data-stu-id="d5d66-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5d66-289"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d5d66-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5d66-290">DLL</span><span class="sxs-lookup"><span data-stu-id="d5d66-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5d66-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5d66-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d66-292">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5d66-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5d66-293">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5d66-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5d66-294">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="d5d66-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

