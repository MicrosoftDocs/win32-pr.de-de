---
description: Die Win32 \_ osherstellyconfiguration&\# 8194; Die WMI-Klasse stellt die Arten von Informationen dar, die beim Ausfall des Betriebssystems aus dem Arbeitsspeicher gesammelt werden. Dies schließt Start Fehler und Systemabstürze ein.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Win32_OSRecoveryConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342776"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="50155-104">Win32 \_ osherstellyconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="50155-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="50155-105">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ oswiederherstellungskonfiguration** stellt die Arten von Informationen dar, die beim Ausfall des Betriebssystems aus dem Arbeitsspeicher gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="50155-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="50155-106">Dies schließt Start Fehler und Systemabstürze ein.</span><span class="sxs-lookup"><span data-stu-id="50155-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="50155-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50155-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="50155-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="50155-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="50155-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="50155-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="50155-110">Member</span><span class="sxs-lookup"><span data-stu-id="50155-110">Members</span></span>

<span data-ttu-id="50155-111">Die **Win32 \_ oswiederherstellungskonfigurations** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="50155-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="50155-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50155-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50155-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50155-113">Properties</span></span>

<span data-ttu-id="50155-114">Die **Win32 \_ osherstellyconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50155-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50155-115">**AutoReboot**</span><span class="sxs-lookup"><span data-stu-id="50155-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50155-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50155-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-118">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot")</span><span class="sxs-lookup"><span data-stu-id="50155-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="50155-119">Das System wird während eines Wiederherstellungs Vorgangs automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="50155-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="50155-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="50155-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50155-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50155-123">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="50155-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="50155-124">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="50155-124">Short textual description of the current object.</span></span>

<span data-ttu-id="50155-125">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50155-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="50155-126">**"Debug filePath"**</span><span class="sxs-lookup"><span data-stu-id="50155-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-129">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| dumpfile")</span><span class="sxs-lookup"><span data-stu-id="50155-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="50155-130">Vollständiger Pfad zur Debugdatei.</span><span class="sxs-lookup"><span data-stu-id="50155-130">Full path to the debug file.</span></span> <span data-ttu-id="50155-131">Eine Debugdatei wird mit dem Speicher Zustand des Computers nach einem Computerfehler erstellt.</span><span class="sxs-lookup"><span data-stu-id="50155-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="50155-132">Beispiel: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="50155-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="50155-133">**DebugInfoType**</span><span class="sxs-lookup"><span data-stu-id="50155-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50155-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50155-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50155-136">Der Typ der Debuginformationen, die in die Protokolldatei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="50155-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="50155-137">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="50155-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="50155-138">**Speicher** Abbild vervollständigen (1)</span><span class="sxs-lookup"><span data-stu-id="50155-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="50155-139">**Kernel Speicher** Abbild (2)</span><span class="sxs-lookup"><span data-stu-id="50155-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="50155-140">**Kleines Speicher** Abbild (3)</span><span class="sxs-lookup"><span data-stu-id="50155-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50155-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50155-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50155-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50155-144">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="50155-144">Textual description of the current object.</span></span>

<span data-ttu-id="50155-145">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50155-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="50155-146">**Expandecoddebug FilePath**</span><span class="sxs-lookup"><span data-stu-id="50155-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50155-149">Erweiterte Version der **DebugFilePath** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="50155-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="50155-150">Beispiel: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="50155-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="50155-151">**Expandecodminidumpdirectory**</span><span class="sxs-lookup"><span data-stu-id="50155-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50155-154">Erweiterte Version der **MiniDumpDirectory** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="50155-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="50155-155">Beispiel: "C: \\ Windows \\ Minidump"</span><span class="sxs-lookup"><span data-stu-id="50155-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="50155-156">**Kerneldumponly**</span><span class="sxs-lookup"><span data-stu-id="50155-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-157">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50155-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50155-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-159">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| kerneldumponly")</span><span class="sxs-lookup"><span data-stu-id="50155-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="50155-160">Nur Kernel-Debuginformationen werden in die Debug-Protokolldatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="50155-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="50155-161">Wenn der Wert **true** ist, wird nur der Zustand des Kernels in eine Datei geschrieben, wenn ein Systemfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="50155-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="50155-162">**False** gibt an, dass das System versucht, den Zustand des Arbeitsspeichers und alle Geräte zu protokollieren, die Informationen über das System bereitstellen können, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="50155-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="50155-163">**MiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="50155-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-166">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| minidumpdir")</span><span class="sxs-lookup"><span data-stu-id="50155-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="50155-167">Verzeichnis, in dem kleine Speicher Abbild Dateien aufgezeichnet und gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="50155-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="50155-168">Beispiel: "% SystemRoot% \\ Minidump"</span><span class="sxs-lookup"><span data-stu-id="50155-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="50155-169">**Name**</span><span class="sxs-lookup"><span data-stu-id="50155-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50155-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50155-172">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="50155-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="50155-173">Der Name für diese Instanz der Win32-Klasse " **\_ osherstellyconfiguration** ".</span><span class="sxs-lookup"><span data-stu-id="50155-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="50155-174">**Overschreiteexistingdebugfile**</span><span class="sxs-lookup"><span data-stu-id="50155-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-175">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50155-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50155-176">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-177">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| Überschreibung")</span><span class="sxs-lookup"><span data-stu-id="50155-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="50155-178">Die neue Debugdatei überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="50155-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="50155-179">**Sendadminalert**</span><span class="sxs-lookup"><span data-stu-id="50155-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50155-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50155-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-182">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| sendalert")</span><span class="sxs-lookup"><span data-stu-id="50155-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="50155-183">Eine Warnmeldung wird im Falle eines Betriebssystem Fehlers an den Systemadministrator gesendet.</span><span class="sxs-lookup"><span data-stu-id="50155-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="50155-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="50155-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50155-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50155-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50155-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50155-187">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="50155-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="50155-188">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="50155-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="50155-189">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50155-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="50155-190">**Schreib debuginfo**</span><span class="sxs-lookup"><span data-stu-id="50155-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-191">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50155-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50155-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-193">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| crashdumpaktivierte")</span><span class="sxs-lookup"><span data-stu-id="50155-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="50155-194">Debuginformationen müssen in eine Protokolldatei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="50155-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="50155-195">**"Write-tosystemlog"**</span><span class="sxs-lookup"><span data-stu-id="50155-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50155-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50155-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50155-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="50155-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="50155-198">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")</span><span class="sxs-lookup"><span data-stu-id="50155-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="50155-199">Ereignisse werden in ein System Protokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="50155-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50155-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50155-200">Remarks</span></span>

<span data-ttu-id="50155-201">Die Win32-Klasse " **\_ osherstellyconfiguration** " ist von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="50155-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50155-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50155-202">Requirements</span></span>



| <span data-ttu-id="50155-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50155-203">Requirement</span></span> | <span data-ttu-id="50155-204">Wert</span><span class="sxs-lookup"><span data-stu-id="50155-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50155-205">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50155-205">Minimum supported client</span></span><br/> | <span data-ttu-id="50155-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50155-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50155-207">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50155-207">Minimum supported server</span></span><br/> | <span data-ttu-id="50155-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50155-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50155-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="50155-209">Namespace</span></span><br/>                | <span data-ttu-id="50155-210">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="50155-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50155-211">MOF</span><span class="sxs-lookup"><span data-stu-id="50155-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50155-212"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="50155-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50155-213">DLL</span><span class="sxs-lookup"><span data-stu-id="50155-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50155-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50155-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50155-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50155-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50155-216">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="50155-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="50155-217">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="50155-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
