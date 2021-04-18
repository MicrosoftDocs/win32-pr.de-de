---
description: Die \_ WMI-Klasse "Win32 processstartup abstract" stellt die Startkonfiguration eines Windows-basierten Prozesses dar.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Win32_ProcessStartup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368282"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="76257-103">Win32- \_ Klasse "processstartup"</span><span class="sxs-lookup"><span data-stu-id="76257-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="76257-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ processstartup** abstract" stellt die Startkonfiguration eines Windows-basierten Prozesses dar.</span><span class="sxs-lookup"><span data-stu-id="76257-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="76257-105">Die-Klasse ist als Methodentyp Definition definiert, was bedeutet, dass Sie nur zum Übergeben von Informationen an die [**Create**](create-method-in-class-win32-process.md) -Methode der [**Win32- \_ Prozess**](win32-process.md) Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76257-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="76257-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="76257-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76257-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76257-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="76257-108">Member</span><span class="sxs-lookup"><span data-stu-id="76257-108">Members</span></span>

<span data-ttu-id="76257-109">Die **Win32 \_ processstartup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="76257-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="76257-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76257-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76257-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76257-111">Properties</span></span>

<span data-ttu-id="76257-112">Die **Win32 \_ processstartup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76257-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76257-113">**"Kreateflags"**</span><span class="sxs-lookup"><span data-stu-id="76257-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-116">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Functions \| [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwkreationflags")</span><span class="sxs-lookup"><span data-stu-id="76257-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="76257-117">Weitere Werte, die die Prioritäts Klasse und die Erstellung des Prozesses steuern.</span><span class="sxs-lookup"><span data-stu-id="76257-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="76257-118">Die folgenden Erstellungs Werte können mit Ausnahme der Angabe in beliebiger Kombination angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="76257-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debuggen \_ Prozess** (1)</span><span class="sxs-lookup"><span data-stu-id="76257-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="76257-120">Wenn dieses Flag festgelegt ist, wird der aufrufende Prozess als Debugger behandelt, und der neue Prozess wird debuggt.</span><span class="sxs-lookup"><span data-stu-id="76257-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="76257-121">Das System benachrichtigt den Debugger über alle Debugereignisse, die beim Debuggen des Prozesses auftreten.</span><span class="sxs-lookup"><span data-stu-id="76257-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="76257-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debuggen \_ Nur \_ dieser \_ Prozess** (2)</span><span class="sxs-lookup"><span data-stu-id="76257-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76257-123">Wenn dieses Flag nicht festgelegt ist und der aufrufende Prozess gedebuggt wird, wird der neue Prozess zu einem anderen Prozess, der gedebuggt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="76257-124">Wenn der aufrufende Prozess nicht debuggt wird, treten keine debuggingbezogenen Aktionen auf.</span><span class="sxs-lookup"><span data-stu-id="76257-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="76257-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Erstellen \_ Sie Angehalten (4** )</span><span class="sxs-lookup"><span data-stu-id="76257-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="76257-126">Der primäre Thread des neuen Prozesses wird in einem angehaltenen Zustand erstellt und wird erst ausgeführt, wenn die [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="76257-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="76257-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Getrennt \_ Prozess** (8)</span><span class="sxs-lookup"><span data-stu-id="76257-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="76257-128">Bei Konsolen Prozessen hat der neue Prozess keinen Zugriff auf die Konsole des übergeordneten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="76257-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="76257-129">Dieses Flag kann nicht verwendet werden, wenn das Flag zum **Erstellen einer \_ neuen \_ Konsole** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76257-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="76257-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Erstellen \_ Sie Neue \_ Konsole** (16)</span><span class="sxs-lookup"><span data-stu-id="76257-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="76257-131">Dieser neue Prozess verfügt über eine neue Konsole, anstatt die übergeordnete Konsole zu erben.</span><span class="sxs-lookup"><span data-stu-id="76257-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="76257-132">Dieses Flag kann nicht mit dem getrennten **\_ prozessflag** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76257-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="76257-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Erstellen \_ Sie Neue \_ Prozess \_ Gruppe** (512)</span><span class="sxs-lookup"><span data-stu-id="76257-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="76257-134">Dieser neue Prozess ist der Stamm Prozess einer neuen Prozessgruppe.</span><span class="sxs-lookup"><span data-stu-id="76257-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="76257-135">Die Prozessgruppe umfasst alle Prozesse, bei denen es sich um nachfolgende Elemente dieses Stamm Prozesses handelt.</span><span class="sxs-lookup"><span data-stu-id="76257-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="76257-136">Der Prozess Bezeichner der neuen Prozessgruppe ist mit dem Prozess Bezeichner identisch, der in der **ProcessID-** Eigenschaft der [**Win32- \_ Prozess**](win32-process.md) Klasse zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76257-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="76257-137">Prozessgruppen werden von der [**generateconsolectrlevent**](/windows/console/generateconsolectrlevent) -Methode verwendet, um das Senden von einem STRG + C-Signal oder einem STRG + UNTBR-Signal an eine Gruppe von Konsolen Prozessen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="76257-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="76257-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Erstellen \_ Sie Unicode- \_ Umgebung** (1024)</span><span class="sxs-lookup"><span data-stu-id="76257-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="76257-139">Die in der Umgebungs **variables** -Eigenschaft aufgelisteten Umgebungseinstellungen verwenden Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="76257-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="76257-140">Wenn dieses Flag nicht festgelegt ist, verwendet der Umgebungsblock ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="76257-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="76257-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Erstellen \_ Sie Standard \_ Fehler \_ Modus** (67108864)</span><span class="sxs-lookup"><span data-stu-id="76257-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="76257-142">Neu erstellte Prozesse erhalten den Standardfehler Modus des aufrufenden Prozesses, anstatt den Fehler Modus des übergeordneten Prozesses zu erben.</span><span class="sxs-lookup"><span data-stu-id="76257-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="76257-143">Dieses Flag eignet sich für multithreadshell-Anwendungen, die mit deaktivierten hart Fehlern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="76257-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="76257-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Erstellen \_ Sie Breakaway \_ von \_ Auftrag** (16777216)</span><span class="sxs-lookup"><span data-stu-id="76257-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="76257-145">Wird für den erstellten Prozess verwendet, der nicht durch das Auftrags Objekt eingeschränkt werden darf.</span><span class="sxs-lookup"><span data-stu-id="76257-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76257-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="76257-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-147">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="76257-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76257-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-149">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="76257-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="76257-150">Liste der Einstellungen für die Konfiguration eines Computers.</span><span class="sxs-lookup"><span data-stu-id="76257-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="76257-151">Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an.</span><span class="sxs-lookup"><span data-stu-id="76257-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="76257-152">Das System verwaltet einen Block von Umgebungseinstellungen für jeden Benutzer und einen für den Computer.</span><span class="sxs-lookup"><span data-stu-id="76257-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="76257-153">Der System Umgebungsblock stellt Umgebungsvariablen für alle Benutzer eines bestimmten Computers dar.</span><span class="sxs-lookup"><span data-stu-id="76257-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="76257-154">Der Umgebungsblock eines Benutzers stellt die Umgebungsvariablen dar, die das System für einen bestimmten Benutzer verwaltet, und enthält den Satz von System Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="76257-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="76257-155">Standardmäßig erhält jeder Prozess eine Kopie des Umgebungs Blocks für seinen übergeordneten Prozess.</span><span class="sxs-lookup"><span data-stu-id="76257-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="76257-156">In der Regel handelt es sich hierbei um den Umgebungsblock für den angemeldeten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="76257-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="76257-157">Von einem Prozess können unterschiedliche Umgebungs Blöcke für die untergeordneten Prozesse angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="76257-158">**Attribut ErrorMode**</span><span class="sxs-lookup"><span data-stu-id="76257-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76257-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76257-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-161">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Error Functions (\* Error Functions \| )")</span><span class="sxs-lookup"><span data-stu-id="76257-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="76257-162">Bei einigen nicht-x86-Prozessoren verursachen falsch ausgerichtete Speicher Verweise eine Ausrichtungsfehler Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="76257-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="76257-163">**\_ \_ \_ Mit Ausnahme von Flag ohne Ausrichtung** können Sie steuern, ob ein Betriebssystem solche Ausrichtungsfehler automatisch korrigiert oder ob Sie für eine Anwendung sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="76257-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="76257-164">Bei einer Plattform für Millionen von Anweisungen pro Sekunde (MIPS) muss eine Anwendung [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) explizit mit dem Flag **No \_ Alignment (keine Ausrichtungs \_ Fehler \_** ) abrufen, damit das Betriebssystem Ausrichtungsfehler automatisch beheben kann.</span><span class="sxs-lookup"><span data-stu-id="76257-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="76257-165">Wie ein Betriebssystem verschiedene Typen von schwerwiegenden Fehlern verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="76257-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="76257-166">Sie können angeben, dass das Betriebssystem Fehler oder eine Anwendung Fehler empfangen und verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="76257-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="76257-167">Die Standardeinstellung ist, dass das Betriebssystem Ausrichtungsfehler für eine Anwendung sichtbar macht.</span><span class="sxs-lookup"><span data-stu-id="76257-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="76257-168">Da die x86-Plattform keine Ausrichtungsfehler für eine Anwendung sichtbar macht, bewirkt der Fehler " **keine \_ Ausrichtung" \_ \_ mit Ausnahme** von Flag nicht, dass das Betriebssystem einen Ausrichtungsfehler ausgelöst hat – auch wenn das Flag nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76257-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="76257-169">Der Standardzustand für [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) besteht darin, alle Flags auf 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="76257-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="76257-170">(1)</span><span class="sxs-lookup"><span data-stu-id="76257-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="76257-171">Standard</span><span class="sxs-lookup"><span data-stu-id="76257-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="76257-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fehler \_ Kritische \_ Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="76257-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76257-173">Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem das Meldungs Feld kritischer Fehlerhandler nicht an, wenn ein solcher Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="76257-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="76257-174">Stattdessen sendet das Betriebssystem den Fehler an den aufrufenden Prozess.</span><span class="sxs-lookup"><span data-stu-id="76257-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="76257-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Nein \_ Ausrichtungs \_ Fehler \_ außer** (4)</span><span class="sxs-lookup"><span data-stu-id="76257-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="76257-176">Wenn dieses Flag festgelegt ist, korrigiert das Betriebssystem automatisch speicherausrichtungsfehler und macht Sie für die Anwendung unsichtbar.</span><span class="sxs-lookup"><span data-stu-id="76257-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="76257-177">Dies erfolgt für die aufrufenden und Nachfolger Prozesse.</span><span class="sxs-lookup"><span data-stu-id="76257-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="76257-178">Dieses Flag gilt nur für das eingeschränkte Anweisungs Satz Computing (RISC) und hat keine Auswirkungen auf x86-Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="76257-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="76257-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Nein \_ \_ \_ Fehler \_ Feld** für den GP-Fehler (8)</span><span class="sxs-lookup"><span data-stu-id="76257-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="76257-180">Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem beim Auftreten eines GP-Fehlers das Fehler Meldungs Feld "allgemeiner Schutz (GP)" nicht an.</span><span class="sxs-lookup"><span data-stu-id="76257-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="76257-181">Dieses Flag sollte nur durch Debuggen von Anwendungen festgelegt werden, die GP-Fehler behandeln.</span><span class="sxs-lookup"><span data-stu-id="76257-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="76257-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Nein \_ \_ \_ Fehler \_ Feld "Datei öffnen** " (16)</span><span class="sxs-lookup"><span data-stu-id="76257-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="76257-183">Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem kein Meldungs Feld an, wenn eine Datei nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="76257-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="76257-184">Stattdessen wird der Fehler an den aufrufenden Prozess zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76257-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="76257-185">Dieses Flag wird zurzeit ignoriert.</span><span class="sxs-lookup"><span data-stu-id="76257-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76257-186">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="76257-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-188">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-189">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwfillattribute")</span><span class="sxs-lookup"><span data-stu-id="76257-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="76257-190">Die Text-und Hintergrundfarben, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="76257-191">Diese Werte werden in grafischen Benutzeroberflächen Anwendungen (GUI) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="76257-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="76257-192">Fügen Sie die Werte hinzu, um Vordergrund-und Hintergrundfarben anzugeben.</span><span class="sxs-lookup"><span data-stu-id="76257-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="76257-193">Wenn Sie z. b. einen roten Typ (4) auf einem blauen Hintergrund (16) haben möchten, legen Sie für FillAttribute den Wert 20 fest.</span><span class="sxs-lookup"><span data-stu-id="76257-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="76257-194">1</span><span class="sxs-lookup"><span data-stu-id="76257-194">1</span></span>
</dt> <dd>

<span data-ttu-id="76257-195">Vordergrund \_ blau</span><span class="sxs-lookup"><span data-stu-id="76257-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="76257-196">2</span><span class="sxs-lookup"><span data-stu-id="76257-196">2</span></span>
</dt> <dd>

<span data-ttu-id="76257-197">Vordergrund \_ grün</span><span class="sxs-lookup"><span data-stu-id="76257-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="76257-198">4</span><span class="sxs-lookup"><span data-stu-id="76257-198">4</span></span>
</dt> <dd>

<span data-ttu-id="76257-199">Vordergrund \_ rot</span><span class="sxs-lookup"><span data-stu-id="76257-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="76257-200">8</span><span class="sxs-lookup"><span data-stu-id="76257-200">8</span></span>
</dt> <dd>

<span data-ttu-id="76257-201">Vordergrund \_ Intensität</span><span class="sxs-lookup"><span data-stu-id="76257-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="76257-202">16</span><span class="sxs-lookup"><span data-stu-id="76257-202">16</span></span>
</dt> <dd>

<span data-ttu-id="76257-203">Hintergrund \_ blau</span><span class="sxs-lookup"><span data-stu-id="76257-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="76257-204">32</span><span class="sxs-lookup"><span data-stu-id="76257-204">32</span></span>
</dt> <dd>

<span data-ttu-id="76257-205">Hintergrund \_ grün</span><span class="sxs-lookup"><span data-stu-id="76257-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="76257-206">64</span><span class="sxs-lookup"><span data-stu-id="76257-206">64</span></span>
</dt> <dd>

<span data-ttu-id="76257-207">\_Roter Hintergrund</span><span class="sxs-lookup"><span data-stu-id="76257-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="76257-208">128</span><span class="sxs-lookup"><span data-stu-id="76257-208">128</span></span>
</dt> <dd>

<span data-ttu-id="76257-209">Hintergrund \_ Intensität</span><span class="sxs-lookup"><span data-stu-id="76257-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76257-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="76257-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-211">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-212">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-213">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**JobObject \_ Basic \_ Limit \_ Information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")</span><span class="sxs-lookup"><span data-stu-id="76257-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="76257-214">Prioritäts Klasse für den neuen Prozess.</span><span class="sxs-lookup"><span data-stu-id="76257-214">Priority class of the new process.</span></span> <span data-ttu-id="76257-215">Verwenden Sie diese Eigenschaft, um die Zeit Plan Prioritäten der Threads im Prozess zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="76257-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="76257-216">Wenn die Eigenschaft den Wert NULL hat, ist die Prioritäts Klasse standardmäßig auf normal –, es sei denn, die Prioritäts Klasse des erstellenden Prozesses ist in Leerlauf oder niedriger \_</span><span class="sxs-lookup"><span data-stu-id="76257-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="76257-217">In diesen Fällen empfängt der untergeordnete Prozess die Standard Prioritäts Klasse des aufrufenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="76257-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="76257-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="76257-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="76257-219">Gibt einen normalen Prozess ohne besondere Zeit Plan Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="76257-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="76257-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>Im **Leerlauf** (64)</span><span class="sxs-lookup"><span data-stu-id="76257-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="76257-221">Gibt einen Prozess mit Threads an, die nur ausgeführt werden, wenn sich das System im Leerlauf befindet und durch die Threads eines Prozesses, der in einer höheren Prioritäts Klasse ausgeführt wird, vorzeitig entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="76257-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="76257-222">Ein Beispiel hierfür ist ein Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="76257-222">An example is a screen saver.</span></span> <span data-ttu-id="76257-223">Die inaktive Prioritäts Klasse wird von untergeordneten Prozessen geerbt.</span><span class="sxs-lookup"><span data-stu-id="76257-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="76257-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (128)</span><span class="sxs-lookup"><span data-stu-id="76257-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="76257-225">Gibt einen Prozess an, der zeitkritische Aufgaben ausführt, die sofort ausgeführt werden müssen, damit Sie ordnungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="76257-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="76257-226">Die Threads eines Klassen Prozesses mit hoher Priorität haben Vorrang vor den Threads der Klassen Prozesse mit normaler Priorität oder der Leerlauf Priorität.</span><span class="sxs-lookup"><span data-stu-id="76257-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="76257-227">Ein Beispiel hierfür ist Windows Aufgabenliste, das beim Aufruf durch den Benutzer schnell reagieren muss, unabhängig von der Last des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="76257-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="76257-228">Verwenden Sie extrem Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, weil eine CPU-gebundene Klasse mit hoher Priorität fast alle verfügbaren Zyklen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="76257-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="76257-229">Nur die echtzeitpriorität wird auf diese Ebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76257-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="76257-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span><span class="sxs-lookup"><span data-stu-id="76257-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="76257-231">Gibt einen Prozess an, der über die höchste mögliche Priorität verfügt.</span><span class="sxs-lookup"><span data-stu-id="76257-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="76257-232">Die Threads eines echt Zeit Prioritäts Klassen Prozesses haben Vorrang vor den Threads aller anderen Prozesse – einschließlich Threads mit hoher Priorität und Betriebssystem Prozessen, die wichtige Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="76257-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="76257-233">Beispielsweise kann ein echt Zeit Prozess, der für mehr als ein sehr kurzes Intervall ausgeführt wird, dazu führen, dass Datenträger Caches nicht geleert werden oder dass die Maus nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="76257-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="76257-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Unten \_ Normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="76257-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="76257-235">Gibt einen Prozess an, der eine Priorität hat, die höher als der Leerlauf, aber niedriger als normal ist.</span><span class="sxs-lookup"><span data-stu-id="76257-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="76257-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Oben \_ Normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="76257-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="76257-237">Gibt einen Prozess an, der eine Priorität hat, die höher als normal, aber kleiner als hoch ist.</span><span class="sxs-lookup"><span data-stu-id="76257-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76257-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="76257-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-239">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76257-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76257-240">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-241">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")</span><span class="sxs-lookup"><span data-stu-id="76257-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="76257-242">Gibt an, wie das Fenster dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-242">How the window is displayed to the user.</span></span> <span data-ttu-id="76257-243">Dabei kann es sich um einen beliebigen Wert handeln, der im *nCmdShow* -Parameter für die [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="76257-243">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="76257-244">**Titel**</span><span class="sxs-lookup"><span data-stu-id="76257-244">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76257-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76257-246">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-246">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-247">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lptitle")</span><span class="sxs-lookup"><span data-stu-id="76257-247">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="76257-248">Text, der in der Titelleiste angezeigt wird, wenn ein neues Konsolenfenster erstellt wird. wird für Konsolen Prozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="76257-248">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="76257-249">Wenn der Wert **null** ist, wird der Name der ausführbaren Datei als Fenstertitel verwendet.</span><span class="sxs-lookup"><span data-stu-id="76257-249">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="76257-250">Diese Eigenschaft muss für GUI-oder Konsolen Prozesse, die kein neues Konsolenfenster erstellen, den Wert **null** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76257-250">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="76257-251">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="76257-251">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76257-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76257-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-253">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-254">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpdesktop")</span><span class="sxs-lookup"><span data-stu-id="76257-254">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="76257-255">Der Name des Desktops oder der Name der Desktop-und Fenster Station für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="76257-255">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="76257-256">Ein umgekehrter Schrägstrich in der Zeichenfolge gibt an, dass die Zeichenfolge sowohl Desktop-als auch Fenster Stationsnamen enthält</span><span class="sxs-lookup"><span data-stu-id="76257-256">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="76257-257">Wenn **WinstationDesktop** **null** ist, erbt der neue Prozess den Desktop und die Fenster Station des übergeordneten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="76257-257">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="76257-258">Wenn **WinstationDesktop** eine leere Zeichenfolge ist, erbt der Prozess nicht den Desktop und die Fenster Station des übergeordneten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="76257-258">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="76257-259">Das System bestimmt, ob eine neue Desktop-und Fenster Station erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="76257-259">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="76257-260">Eine Fenster Station ist ein sicheres Objekt, das eine Zwischenablage, eine Reihe globaler Atome und eine Gruppe von Desktop Objekten enthält.</span><span class="sxs-lookup"><span data-stu-id="76257-260">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="76257-261">Die interaktive Fenster Station, die der Anmelde Sitzung des interaktiven Benutzers zugewiesen ist, enthält auch das Tastatur-, Maus-und Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="76257-261">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="76257-262">Ein Desktop ist ein sicheres Objekt, das in einer Fenster Station enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="76257-262">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="76257-263">Ein Desktop verfügt über eine logische Anzeige Oberfläche und enthält Fenster, Menüs und Hooks.</span><span class="sxs-lookup"><span data-stu-id="76257-263">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="76257-264">Eine Fenster Station kann über mehrere Desktops verfügen.</span><span class="sxs-lookup"><span data-stu-id="76257-264">A window station can have multiple desktops.</span></span> <span data-ttu-id="76257-265">Nur die Desktops der interaktiven Fenster Station können sichtbar sein und Benutzereingaben empfangen.</span><span class="sxs-lookup"><span data-stu-id="76257-265">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="76257-266">**X**</span><span class="sxs-lookup"><span data-stu-id="76257-266">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-267">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-268">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-269">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| DWX")</span><span class="sxs-lookup"><span data-stu-id="76257-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="76257-270">Der X-Offset der oberen linken Ecke eines Fensters, wenn ein neues Fenster erstellt wird – in Pixel.</span><span class="sxs-lookup"><span data-stu-id="76257-270">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="76257-271">Die Offsets befinden sich in der oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="76257-271">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="76257-272">Bei GUI-Prozessen wird die angegebene Position verwendet, wenn der neue Prozess zum ersten Mal das überlappende [**Fenster aufruft,**](/windows/win32/api/winuser/nf-winuser-createwindowa) um ein überlappendes Fenster zu erstellen, wenn der *X* -Parameter von "up **Window** " den Wert **CW \_ usedefault** hat.</span><span class="sxs-lookup"><span data-stu-id="76257-272">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="76257-273">\[! Hinweis X\]</span><span class="sxs-lookup"><span data-stu-id="76257-273">\[!Note  X\]</span></span>  
> <span data-ttu-id="76257-274">und **Y** können nicht unabhängig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-274">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="76257-275">**Xcountrytchars**</span><span class="sxs-lookup"><span data-stu-id="76257-275">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-276">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-276">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-277">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-278">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| xcountrytchars")</span><span class="sxs-lookup"><span data-stu-id="76257-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="76257-279">Breite des Bildschirm Puffers in Zeichen Spalten.</span><span class="sxs-lookup"><span data-stu-id="76257-279">Screen buffer width in character columns.</span></span> <span data-ttu-id="76257-280">Diese Eigenschaft wird für Prozesse verwendet, die ein Konsolenfenster erstellen, und wird in GUI-Prozessen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="76257-280">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="76257-281">**Xzähltchars** und **yzähltchars** können nicht unabhängig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-281">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="76257-282">**Xsize**</span><span class="sxs-lookup"><span data-stu-id="76257-282">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-284">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-285">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwxsize")</span><span class="sxs-lookup"><span data-stu-id="76257-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="76257-286">Pixel Breite eines Fensters, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-286">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="76257-287">Für GUI-Prozesse wird dies nur verwendet, wenn der neue [**Prozess zum ersten**](/windows/win32/api/winuser/nf-winuser-createwindowa) Mal das überlappende Fenster aufruft, um ein überlappendes Fenster zu erstellen, wenn der nwidth-Parameter von "up **Window** " den Wert **CW \_ usedefault** hat.</span><span class="sxs-lookup"><span data-stu-id="76257-287">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="76257-288">**XSize** und **YSize** können nicht unabhängig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-288">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="76257-289">**J**</span><span class="sxs-lookup"><span data-stu-id="76257-289">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-290">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-291">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-291">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-292">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwy")</span><span class="sxs-lookup"><span data-stu-id="76257-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="76257-293">Der Pixel Offset der oberen linken Ecke eines Fensters, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-293">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="76257-294">Die Offsets befinden sich in der oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="76257-294">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="76257-295">Bei GUI-Prozessen wird die angegebene Position verwendet, wenn der neue Prozess zum ersten Mal das überlappende [**Fenster aufruft,**](/windows/win32/api/winuser/nf-winuser-createwindowa) um ein überlappendes Fenster zu erstellen, wenn der *y* -Parameter von "up **Window** " den Wert **CW \_ usedefault** hat.</span><span class="sxs-lookup"><span data-stu-id="76257-295">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="76257-296">\[! Hinweis X\]</span><span class="sxs-lookup"><span data-stu-id="76257-296">\[!Note  X\]</span></span>  
> <span data-ttu-id="76257-297">und **Y** können nicht unabhängig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-297">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="76257-298">**Ycountrytchars**</span><span class="sxs-lookup"><span data-stu-id="76257-298">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-299">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-300">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-301">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| yzähltchars")</span><span class="sxs-lookup"><span data-stu-id="76257-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="76257-302">Höhe des Bildschirm Puffers in Zeichen Zeilen.</span><span class="sxs-lookup"><span data-stu-id="76257-302">Screen buffer height in character rows.</span></span> <span data-ttu-id="76257-303">Diese Eigenschaft wird für Prozesse verwendet, die ein Konsolenfenster erstellen, wird jedoch in GUI-Prozessen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="76257-303">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="76257-304">**Xzähltchars** und **yzähltchars** können nicht unabhängig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-304">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="76257-305">**Ysize**</span><span class="sxs-lookup"><span data-stu-id="76257-305">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76257-306">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76257-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76257-307">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="76257-307">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76257-308">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwysize")</span><span class="sxs-lookup"><span data-stu-id="76257-308">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="76257-309">Die Pixelhöhe eines Fensters, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-309">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="76257-310">Für GUI-Prozesse wird dies nur beim ersten Aufrufen von " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " durch den neuen Prozess zum Erstellen eines überlappenden Fensters verwendet, wenn der *nwidth* -Parameter von "up **Window** " den Wert " **CW \_ usedefault**" hat.</span><span class="sxs-lookup"><span data-stu-id="76257-310">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="76257-311">**XSize** und **YSize** können nicht unabhängig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76257-311">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76257-312">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76257-312">Remarks</span></span>

<span data-ttu-id="76257-313">Diese Klasse wird von [**Win32 \_ methodparameterclass**](win32-methodparameterclass.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="76257-313">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="76257-314">Übersicht</span><span class="sxs-lookup"><span data-stu-id="76257-314">Overview</span></span>

<span data-ttu-id="76257-315">Die [**Win32 \_ Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) -Methode ermöglicht Ihnen das Konfigurieren von Startoptionen für jeden neuen Prozess, der auf einem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76257-315">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="76257-316">Beispielsweise können Sie einen Prozess so konfigurieren, dass er in einem "ausgeblendeten" Fenster gestartet wird. Dadurch wird verhindert, dass ein Benutzer es sieht und möglicherweise unterbricht.</span><span class="sxs-lookup"><span data-stu-id="76257-316">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="76257-317">Wenn der Prozess in einem Befehlsfenster ausgeführt wird, können Sie Größe, Titel und Vordergrund-und Hintergrundfarben des Fensters konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="76257-317">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="76257-318">Startoptionen werden mithilfe der Win32-Klasse " **\_ processstartup** " konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="76257-318">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="76257-319">**Win32 \_ Processstartup** ist eine Klasse vom Typ "Methode". die Type-Methode der Methode ist nur vorhanden, um Informationen an eine Methode zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="76257-319">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="76257-320">In diesem Fall werden alle Eigenschaften einer Instanz von **Win32 \_ processstartup** an eine Instanz des [**Win32- \_ Prozesses**](win32-process.md)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="76257-320">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="76257-321">**Verwenden von Win32 \_ processstartup**</span><span class="sxs-lookup"><span data-stu-id="76257-321">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="76257-322">Erstellen Sie eine Instanz von **Win32 \_ processstartup**.</span><span class="sxs-lookup"><span data-stu-id="76257-322">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="76257-323">Konfigurieren Sie die Eigenschaften der neuen Instanz.</span><span class="sxs-lookup"><span data-stu-id="76257-323">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="76257-324">Fügen Sie die-Instanz als Teil der [**Win32 \_ Process**](win32-process.md) Create-Methode ein.</span><span class="sxs-lookup"><span data-stu-id="76257-324">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="76257-325">Wenn Sie z. b. eine **Win32- \_ processstartup** -Instanz mit dem Namen objconfig erstellt haben, würden Sie den Objektnamen in der Create-Methode wie folgt übergeben:</span><span class="sxs-lookup"><span data-stu-id="76257-325">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="76257-326">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76257-326">Examples</span></span>

<span data-ttu-id="76257-327">Sie können die **Win32 \_ processstartup** -Klasse verwenden, um verschiedene Startoptionen für einen Prozess zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="76257-327">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="76257-328">Zu diesen Optionen zählen unter anderem das Erstellen eines Prozesses in einem ausgeblendeten Fenster und das Erstellen eines Prozesses mit höherer Priorität.</span><span class="sxs-lookup"><span data-stu-id="76257-328">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="76257-329">Mit dem folgenden VBScript wird ein Prozess in einem verborgenen Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="76257-329">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="76257-330">Das folgende VBScript-Objekt erstellt einen Prozess mit höherer Priorität.</span><span class="sxs-lookup"><span data-stu-id="76257-330">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="76257-331">Im folgenden VBScript-Codebeispiel wird ein Notepad-Prozess auf dem lokalen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="76257-331">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="76257-332">**Win32 \_ Processstartup** wird verwendet, um die Prozesseinstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="76257-332">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="76257-333">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76257-333">Requirements</span></span>



| <span data-ttu-id="76257-334">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76257-334">Requirement</span></span> | <span data-ttu-id="76257-335">Wert</span><span class="sxs-lookup"><span data-stu-id="76257-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76257-336">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76257-336">Minimum supported client</span></span><br/> | <span data-ttu-id="76257-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76257-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76257-338">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76257-338">Minimum supported server</span></span><br/> | <span data-ttu-id="76257-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76257-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76257-340">Namespace</span><span class="sxs-lookup"><span data-stu-id="76257-340">Namespace</span></span><br/>                | <span data-ttu-id="76257-341">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="76257-341">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76257-342">MOF</span><span class="sxs-lookup"><span data-stu-id="76257-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76257-343"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="76257-343"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76257-344">DLL</span><span class="sxs-lookup"><span data-stu-id="76257-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76257-345"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76257-345"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76257-346">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76257-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76257-347">**Win32 \_ methodparameterclass**</span><span class="sxs-lookup"><span data-stu-id="76257-347">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="76257-348">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="76257-348">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="76257-349">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="76257-349">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="76257-350">**\_\_Providerhostquotaconfiguration**</span><span class="sxs-lookup"><span data-stu-id="76257-350">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="76257-351">WMI-Tasks: Prozesse</span><span class="sxs-lookup"><span data-stu-id="76257-351">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
