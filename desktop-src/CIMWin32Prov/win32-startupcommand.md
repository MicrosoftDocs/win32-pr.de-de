---
description: Der Win32- \_ startupcommand&\# 8194; WMI-Klasse stellt einen Befehl dar, der automatisch ausgeführt wird, wenn sich ein Benutzer auf dem Computersystem anmeldet.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Win32_StartupCommand-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861580"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="996aa-103">Win32- \_ startupcommand-Klasse</span><span class="sxs-lookup"><span data-stu-id="996aa-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="996aa-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ startupcommand** stellt einen Befehl dar, der automatisch ausgeführt wird, wenn sich ein Benutzer am Computersystem anmeldet.</span><span class="sxs-lookup"><span data-stu-id="996aa-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="996aa-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="996aa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="996aa-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="996aa-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="996aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="996aa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="996aa-108">Member</span><span class="sxs-lookup"><span data-stu-id="996aa-108">Members</span></span>

<span data-ttu-id="996aa-109">Die **Win32 \_ startupcommand** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="996aa-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="996aa-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="996aa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="996aa-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="996aa-111">Properties</span></span>

<span data-ttu-id="996aa-112">Die **Win32 \_ startupcommand** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="996aa-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="996aa-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="996aa-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="996aa-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="996aa-117">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="996aa-117">Short textual description of the current object.</span></span>

<span data-ttu-id="996aa-118">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="996aa-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="996aa-119">**Befehl**</span><span class="sxs-lookup"><span data-stu-id="996aa-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-122">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="996aa-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="996aa-123">Befehl, der vom Startbefehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="996aa-123">Command run by the startup command.</span></span>

<span data-ttu-id="996aa-124">WMI erhält diese Daten aus dem Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="996aa-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="996aa-125">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**</span><span class="sxs-lookup"><span data-stu-id="996aa-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="996aa-126">Beispiel: "C: \\ Windows \\notepad.exe myfile.txt"</span><span class="sxs-lookup"><span data-stu-id="996aa-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="996aa-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="996aa-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="996aa-130">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="996aa-130">Textual description of the current object.</span></span>

<span data-ttu-id="996aa-131">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="996aa-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="996aa-132">**Location**</span><span class="sxs-lookup"><span data-stu-id="996aa-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-135">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Windows")</span><span class="sxs-lookup"><span data-stu-id="996aa-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="996aa-136">Der Pfad, in dem sich der Startbefehl auf dem Dateisystem befindet.</span><span class="sxs-lookup"><span data-stu-id="996aa-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="996aa-137">Beispiel: HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="996aa-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="996aa-138">**Start** ("Startup")</span><span class="sxs-lookup"><span data-stu-id="996aa-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="996aa-139">**Gemeinsamer Start** ("gemeinsamer Start")</span><span class="sxs-lookup"><span data-stu-id="996aa-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="996aa-140">**HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="996aa-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="996aa-141">**HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")</span><span class="sxs-lookup"><span data-stu-id="996aa-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="996aa-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="996aa-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-145">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")</span><span class="sxs-lookup"><span data-stu-id="996aa-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="996aa-146">Der Dateiname des Start Befehls.</span><span class="sxs-lookup"><span data-stu-id="996aa-146">File name of the startup command.</span></span>

<span data-ttu-id="996aa-147">Beispiel: "findfast"</span><span class="sxs-lookup"><span data-stu-id="996aa-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="996aa-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="996aa-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-151">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="996aa-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="996aa-152">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="996aa-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="996aa-153">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="996aa-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="996aa-154">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="996aa-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-157">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="996aa-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="996aa-158">Der Benutzername, für den dieser Startbefehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="996aa-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="996aa-159">Beispiel: "mydomain \\ myname"</span><span class="sxs-lookup"><span data-stu-id="996aa-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="996aa-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="996aa-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996aa-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="996aa-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="996aa-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996aa-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996aa-163">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="996aa-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="996aa-164">Die UserSID-Eigenschaft gibt die SID des Benutzers an, für den dieser Startbefehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="996aa-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="996aa-165">Diese Benutzer Eigenschaft ist möglicherweise leer, aber die UserSID hat weiterhin einen Wert, wenn der Benutzername nicht aufgelöst werden kann (z. b. im Fall eines gelöschten Benutzers).</span><span class="sxs-lookup"><span data-stu-id="996aa-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="996aa-166">Die-Eigenschaft ist hilfreich, um zwischen den Befehlen zu unterscheiden, die mit nicht aufgelösten, nicht aufgelösten, nicht</span><span class="sxs-lookup"><span data-stu-id="996aa-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="996aa-167">Dieser Wert kann NULL sein, wenn der Befehl Elementen zugeordnet ist, die einen Benutzer nicht wie alle Benutzer identifizieren.</span><span class="sxs-lookup"><span data-stu-id="996aa-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="996aa-168">Beispiel: S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="996aa-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="996aa-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="996aa-169">Remarks</span></span>

<span data-ttu-id="996aa-170">Die **Win32-Klasse \_ startupcommand** ist von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="996aa-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="996aa-171">Das Starten des Computers endet nicht, nachdem das Betriebssystem geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="996aa-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="996aa-172">Stattdessen kann das Windows-Betriebssystem so konfiguriert werden, dass Start Befehle bei jedem Start von Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="996aa-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="996aa-173">Start Befehle werden in der Registrierung oder als Teil des Benutzerprofils gespeichert und zum automatischen Starten angegebener Skripts oder Anwendungen bei jedem Laden von Windows verwendet.</span><span class="sxs-lookup"><span data-stu-id="996aa-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="996aa-174">In den meisten Fällen sind Autostart-Programme nützlich. Sie stellen sicher, dass bestimmte Anwendungen, z. b. Antivirussoftware, beim Laden von Fenstern automatisch gestartet und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="996aa-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="996aa-175">Autostart-Programme können jedoch auch für Probleme verantwortlich sein, z. b.:</span><span class="sxs-lookup"><span data-stu-id="996aa-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="996aa-176">Computer, deren Start sehr viel Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="996aa-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="996aa-177">Dies kann auf eine große Anzahl von Anwendungen zurückzuführen sein, die bei jedem Start von Windows gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="996aa-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="996aa-178">Anwendungen, die in der Taskleiste oder im Task-Manager dargestellt werden, auch wenn der Benutzer Sie nicht gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="996aa-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="996aa-179">Obwohl diese Anwendungen nicht zwangsläufig Probleme verursachen, kann dies dazu führen, dass Helpdeskmitarbeiter von Benutzern, die nicht wissen, woher diese Programme stammen und warum Sie ausgeführt werden, dazu führen können.</span><span class="sxs-lookup"><span data-stu-id="996aa-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="996aa-180">Computer, die Probleme haben, auch wenn Sie sich im Leerlauf befinden.</span><span class="sxs-lookup"><span data-stu-id="996aa-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="996aa-181">Diese Probleme sind häufig auf Start Befehle zurückzuführen, die ausgeführt werden, wenn niemand weiß, dass Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="996aa-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="996aa-182">Das Identifizieren der Anwendungen und Skripts, die beim Start automatisch ausgeführt werden, ist eine wichtige, aber schwierige administrative Aufgabe, da Start Befehle an vielen verschiedenen Speicherorten gespeichert werden können:</span><span class="sxs-lookup"><span data-stu-id="996aa-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="996aa-183">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="996aa-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="996aa-184">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="996aa-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="996aa-185">HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="996aa-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="996aa-186">HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="996aa-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="996aa-187">HKU \\ ProgID \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="996aa-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="996aa-188">System Drive \\ Dokumente und Einstellungen \\ alle Benutzer \\ Start Menü \\ Programme \\ starten</span><span class="sxs-lookup"><span data-stu-id="996aa-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="996aa-189">System Drive \\ Documents and Settings \\ username \\ Startmenü \\ Programme \\ Startup</span><span class="sxs-lookup"><span data-stu-id="996aa-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="996aa-190">Sie können die WMI-Win32- \_ startupcommand-Klasse verwenden, um Autostart-Programme unabhängig davon aufzulisten, wo die Informationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="996aa-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="996aa-191">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="996aa-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="996aa-192">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="996aa-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="996aa-193">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="996aa-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="996aa-194">Sie können die Registrierungs Werte ändern, wenn **Win32 \_ startupcommand** Daten abruft, indem Sie die Methoden der WMI- [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) in Skripts oder in C++ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="996aa-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="996aa-195">Weitere Informationen finden Sie unter [Ändern der System Registrierung](../wmisdk/modifying-the-system-registry.md).</span><span class="sxs-lookup"><span data-stu-id="996aa-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="996aa-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="996aa-196">Examples</span></span>

<span data-ttu-id="996aa-197">Das folgende VBScript listet die Start Befehle auf einem Computer auf.</span><span class="sxs-lookup"><span data-stu-id="996aa-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="996aa-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="996aa-198">Requirements</span></span>



| <span data-ttu-id="996aa-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="996aa-199">Requirement</span></span> | <span data-ttu-id="996aa-200">Wert</span><span class="sxs-lookup"><span data-stu-id="996aa-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="996aa-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="996aa-201">Minimum supported client</span></span><br/> | <span data-ttu-id="996aa-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="996aa-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="996aa-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="996aa-203">Minimum supported server</span></span><br/> | <span data-ttu-id="996aa-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="996aa-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="996aa-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="996aa-205">Namespace</span></span><br/>                | <span data-ttu-id="996aa-206">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="996aa-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="996aa-207">MOF</span><span class="sxs-lookup"><span data-stu-id="996aa-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="996aa-208"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="996aa-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="996aa-209">DLL</span><span class="sxs-lookup"><span data-stu-id="996aa-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="996aa-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="996aa-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996aa-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="996aa-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996aa-212">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="996aa-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="996aa-213">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="996aa-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
