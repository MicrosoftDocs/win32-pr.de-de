---
description: Die \_ WMI-Klasse "Win32 wmisetting Singleton" enthält die Betriebsparameter für den WMI-Dienst. Diese Klasse kann nur über eine Instanz verfügen, die für jedes Windows-System immer vorhanden ist und nicht gelöscht werden kann. Es können keine zusätzlichen Instanzen erstellt werden.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860683"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="38780-105">Win32 \_ wmisetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="38780-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="38780-106">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ wmisetting** Singleton" enthält die Betriebsparameter für den WMI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="38780-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="38780-107">Diese Klasse kann nur über eine Instanz verfügen, die für jedes Windows-System immer vorhanden ist und nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="38780-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="38780-108">Es können keine zusätzlichen Instanzen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="38780-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="38780-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="38780-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="38780-110">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="38780-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38780-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="38780-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="38780-112">Member</span><span class="sxs-lookup"><span data-stu-id="38780-112">Members</span></span>

<span data-ttu-id="38780-113">Die **Win32 \_ wmisetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="38780-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="38780-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38780-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38780-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38780-115">Properties</span></span>

<span data-ttu-id="38780-116">Die **Win32 \_ wmisetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="38780-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38780-117">**ASPScriptDefaultNamespace**</span><span class="sxs-lookup"><span data-stu-id="38780-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-120">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| Standard Namespace")</span><span class="sxs-lookup"><span data-stu-id="38780-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="38780-121">Standardmäßiger Skript Namespace.</span><span class="sxs-lookup"><span data-stu-id="38780-121">Default script namespace.</span></span> <span data-ttu-id="38780-122">Diese Eigenschaft enthält den Namespace, der von Aufrufen von der Skript-API für WMI verwendet wird, wenn keine vom Aufrufer angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="38780-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="38780-123">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-124">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting \| Standard Namespace**    </span><span class="sxs-lookup"><span data-stu-id="38780-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="38780-125">Beispiel: root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="38780-125">Example: root\\cimv2</span></span>

<span data-ttu-id="38780-126">Ein Beispielskript, in dem diese Eigenschaft verwendet wird, finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="38780-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="38780-127">**ASPScriptEnabled**</span><span class="sxs-lookup"><span data-stu-id="38780-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="38780-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38780-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-130">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| enable for ASP")</span><span class="sxs-lookup"><span data-stu-id="38780-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="38780-131">**True** gibt an, dass WMI-Skripting auf Active Server Seiten (ASP) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="38780-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="38780-132">Diese Eigenschaft gilt nur für Systeme, die nur nicht unterstützte Versionen von Windows ausführen.</span><span class="sxs-lookup"><span data-stu-id="38780-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="38780-133">Für unterstützte Windows-Systeme ist die WMI-Skripterstellung in ASP immer zulässig.</span><span class="sxs-lookup"><span data-stu-id="38780-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="38780-134">**Autorecovermufs**</span><span class="sxs-lookup"><span data-stu-id="38780-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-135">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="38780-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38780-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-137">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutoRecover mufs")</span><span class="sxs-lookup"><span data-stu-id="38780-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="38780-138">Liste der voll qualifizierten MOF-Dateinamen, die zum Initialisieren oder Wiederherstellen des WMI-Repository verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38780-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="38780-139">Die Liste legt die Reihenfolge fest, in der MOF-Dateien kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="38780-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="38780-140">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-141">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| AutoRecover-mufs**    </span><span class="sxs-lookup"><span data-stu-id="38780-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="38780-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="38780-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-145">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")</span><span class="sxs-lookup"><span data-stu-id="38780-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="38780-146">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38780-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="38780-147">**Nicht starten** (0)</span><span class="sxs-lookup"><span data-stu-id="38780-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="38780-148">**Autostart** (1)</span><span class="sxs-lookup"><span data-stu-id="38780-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="38780-149">**Beim Neustart starten** (2)</span><span class="sxs-lookup"><span data-stu-id="38780-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38780-150">**Sicherungs Intervall umfasst**</span><span class="sxs-lookup"><span data-stu-id="38780-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-153">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("Minutes")</span><span class="sxs-lookup"><span data-stu-id="38780-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="38780-154">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38780-154">Not supported.</span></span> <span data-ttu-id="38780-155">Sichern Sie das WMI-Repository stattdessen manuell.</span><span class="sxs-lookup"><span data-stu-id="38780-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="38780-156">**BackupLastTime**</span><span class="sxs-lookup"><span data-stu-id="38780-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-157">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="38780-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="38780-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-159">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Functions \| GetTimeZoneInformation")</span><span class="sxs-lookup"><span data-stu-id="38780-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="38780-160">Datum und Uhrzeit der letzten Sicherung.</span><span class="sxs-lookup"><span data-stu-id="38780-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="38780-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="38780-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-164">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build")</span><span class="sxs-lookup"><span data-stu-id="38780-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="38780-165">Versionsinformationen für den aktuell installierten WMI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="38780-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="38780-166">Zeitspanne zwischen Sicherungen der WMI-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="38780-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="38780-167">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-168">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| Build**</span><span class="sxs-lookup"><span data-stu-id="38780-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="38780-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="38780-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-172">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="38780-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="38780-173">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="38780-173">Short textual description of the current object.</span></span>

<span data-ttu-id="38780-174">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="38780-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="38780-175">**DatabaseDirectory**</span><span class="sxs-lookup"><span data-stu-id="38780-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-178">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Repository Directory")</span><span class="sxs-lookup"><span data-stu-id="38780-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="38780-179">Verzeichnispfad, der das WMI-Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="38780-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="38780-180">**Databasemaxsize**</span><span class="sxs-lookup"><span data-stu-id="38780-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-181">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-183">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB Size"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="38780-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="38780-184">Maximale Größe des WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="38780-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="38780-185">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38780-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38780-188">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="38780-188">Textual description of the current object.</span></span>

<span data-ttu-id="38780-189">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="38780-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="38780-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="38780-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-191">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="38780-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38780-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-193">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| enableanonconnections")</span><span class="sxs-lookup"><span data-stu-id="38780-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="38780-194">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38780-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="38780-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="38780-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="38780-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38780-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-198">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| enableEvents")</span><span class="sxs-lookup"><span data-stu-id="38780-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="38780-199">**True** gibt an, dass das WMI-Ereignis Subsystem aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38780-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="38780-200">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-201">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="38780-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="38780-202">**EnableStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="38780-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-203">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="38780-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38780-204">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-205">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")</span><span class="sxs-lookup"><span data-stu-id="38780-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="38780-206">**True** gibt an, dass WMI einen vorab zugeordneten Heap mit der Größe des **LastStartupHeapPreallocation** -Werts erstellt, wenn WMI initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="38780-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="38780-207">**Highdie oldonclientobjects**</span><span class="sxs-lookup"><span data-stu-id="38780-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-209">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-210">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("Objects per Second")</span><span class="sxs-lookup"><span data-stu-id="38780-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="38780-211">Maximale Rate, mit der vom Anbieter erstellte Objekte an Clients übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="38780-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="38780-212">Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, hält WMI Objekte in Warteschlangen vor der Übermittlung an Consumer.</span><span class="sxs-lookup"><span data-stu-id="38780-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="38780-213">Zur Steigerung der Effizienz müssen die Consumer die Objekte in einem Tempo erfassen, das mit dem Anbieter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="38780-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="38780-214">Wenn der Speicher, der von nicht erfassten Objekten belegt wird, **Lowder oldonobjects** erreicht, verlangsamt WMI das Hinzufügen neuer Objekte in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="38780-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="38780-215">Wenn nicht erfasste Ereignisse weiterhin gesammelt werden und die maximale Wartezeit für das Übermitteln von Ereignissen in **maxwaitonclientobjects** erreicht wird, während der verwendete Arbeitsspeicher den Wert in **highationsoldonclientobjects** hat, nimmt WMI keine weiteren Objekte von Anbietern an und gibt **WBEM \_ E aus dem Arbeits \_ \_ \_ Speicher** an die Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="38780-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="38780-216">**Highderoldonevents**</span><span class="sxs-lookup"><span data-stu-id="38780-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-217">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-218">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-219">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Ereignisse pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="38780-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="38780-220">Maximale Rate, mit der Ereignisse an Clients übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="38780-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="38780-221">Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, werden Ereignisse in der WMI-Warteschlange vor der Übermittlung an Consumer</span><span class="sxs-lookup"><span data-stu-id="38780-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="38780-222">Zur Steigerung der Effizienz müssen die Consumer die Ereignisse in einem Tempo erfassen, das mit dem Anbieter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="38780-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="38780-223">Wenn der Speicher, der von nicht gesammelten Ereignissen belegt wird, **Lowder oldonobjects** erreicht, verlangsamt WMI das Hinzufügen neuer Ereignisse in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="38780-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="38780-224">Wenn nicht gesammelte Ereignisse weiterhin kumuliert werden und die maximale Wartezeit für das Übermitteln von Ereignissen in **maxwaitonevents** erreicht wird, während der verwendete Arbeitsspeicher den Wert in **highationsoldonevents** hat, akzeptiert WMI keine weiteren Ereignisse von Anbietern und gibt **WBEM E nicht mehr den Arbeits \_ \_ \_ \_ Speicher** an die Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="38780-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="38780-225">Die Drosselung wird nur für permanente Ereignisconsumer durchgeführt, sodass temporäre Consumer keine Drosselung erwarten sollten, wenn Ereignisse in der internen WMI-Ereignis Warteschlange gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="38780-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="38780-226">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-227">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects (B)**    </span><span class="sxs-lookup"><span data-stu-id="38780-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="38780-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="38780-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-231">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM- \| Installationsverzeichnis")</span><span class="sxs-lookup"><span data-stu-id="38780-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="38780-232">Verzeichnispfad, in dem die WMI-Software installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="38780-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="38780-233">Der Standard Speicherort ist \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="38780-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="38780-234">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-235">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM- \| Installationsverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="38780-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="38780-236">**LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="38780-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-237">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-239">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="38780-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="38780-240">Größe des vorab zugeordneten Heaps, der während der Initialisierung von WMI erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="38780-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="38780-241">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-242">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="38780-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="38780-243">**Loggingdirectory**</span><span class="sxs-lookup"><span data-stu-id="38780-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-245">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-246">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")</span><span class="sxs-lookup"><span data-stu-id="38780-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="38780-247">Verzeichnispfad, der den Speicherort der WMI-System Protokolldateien enthält.</span><span class="sxs-lookup"><span data-stu-id="38780-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="38780-248">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-249">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM- \| Protokollierungs Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="38780-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="38780-250">**LoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="38780-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-251">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-252">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-253">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging")</span><span class="sxs-lookup"><span data-stu-id="38780-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="38780-254">Aktivieren der Ereignisprotokollierung und des ausführlichkeits Grads der verwendeten Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="38780-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="38780-255">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-256">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM- \| Protokollierung**</span><span class="sxs-lookup"><span data-stu-id="38780-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="38780-257">**Aus** (0)</span><span class="sxs-lookup"><span data-stu-id="38780-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="38780-258">**Fehler Protokollierung** (1)</span><span class="sxs-lookup"><span data-stu-id="38780-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="38780-259">Ausführliche **Fehler Protokollierung** (2)</span><span class="sxs-lookup"><span data-stu-id="38780-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38780-260">**Lowder oldonclientobjects**</span><span class="sxs-lookup"><span data-stu-id="38780-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-261">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-263">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("Objects per Second")</span><span class="sxs-lookup"><span data-stu-id="38780-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="38780-264">Rate, mit der WMI die Erstellung neuer Objekte verlangsamt, die für-Clients erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="38780-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="38780-265">Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, hält WMI Objekte in Warteschlangen vor der Übermittlung an Consumer.</span><span class="sxs-lookup"><span data-stu-id="38780-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="38780-266">Zur Steigerung der Effizienz müssen die Consumer die Objekte in einem Tempo erfassen, das mit dem Anbieter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="38780-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="38780-267">Wenn die Anforderungs Rate von Objekten **lowationsoldonclientobjects** erreicht, verlangsamt WMI schrittweise die Erstellung neuer Objekte entsprechend der Verwendungsrate des Clients.</span><span class="sxs-lookup"><span data-stu-id="38780-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="38780-268">Diese Verlangsamung beginnt, wenn die Rate, mit der Objekte erstellt werden, den Wert dieser Eigenschaft überschreitet.</span><span class="sxs-lookup"><span data-stu-id="38780-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="38780-269">Siehe **highdie oldonclientobjects**.</span><span class="sxs-lookup"><span data-stu-id="38780-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="38780-270">Diese Eigenschaft gibt den Registrierungs Wert wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-270">This property reflects the registry value.</span></span>

<span data-ttu-id="38780-271">**Schlüssel \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects (B)**    </span><span class="sxs-lookup"><span data-stu-id="38780-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="38780-272">**Lowdie oldonevents**</span><span class="sxs-lookup"><span data-stu-id="38780-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-275">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Ereignisse pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="38780-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="38780-276">Rate, mit der WMI die Übermittlung neuer Ereignisse verlangsamt.</span><span class="sxs-lookup"><span data-stu-id="38780-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="38780-277">Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, werden Ereignisse in der WMI-Warteschlange vor der Übermittlung an Consumer</span><span class="sxs-lookup"><span data-stu-id="38780-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="38780-278">Zur Steigerung der Effizienz müssen die Consumer die Objekte in einem Tempo erfassen, das mit dem Anbieter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="38780-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="38780-279">Wenn die Warteschlange nicht mehr von der Kontrolle ist, wird die WMI-Drosselung – verlangsamt – die Bereitstellung von Ereignissen nach und nach mit der Client Rate.</span><span class="sxs-lookup"><span data-stu-id="38780-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="38780-280">Diese Verlangsamung beginnt, wenn die Rate, mit der Ereignisse generiert werden, den Wert dieser Eigenschaft überschreitet.</span><span class="sxs-lookup"><span data-stu-id="38780-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="38780-281">Siehe **highdie oldonevents**.</span><span class="sxs-lookup"><span data-stu-id="38780-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="38780-282">Die Drosselung wird nur für permanente Ereignisconsumer durchgeführt, sodass temporäre Consumer keine Drosselung erwarten sollten, wenn Ereignisse in der internen WMI-Ereignis Warteschlange gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="38780-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="38780-283">Diese Eigenschaft gibt den Registrierungs Wert wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-283">This property reflects the registry value.</span></span>

<span data-ttu-id="38780-284">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects {B}**    </span><span class="sxs-lookup"><span data-stu-id="38780-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="38780-285">**MaxLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="38780-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-286">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-287">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-288">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log file max size"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="38780-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="38780-289">Maximale Größe der Protokolldateien, die vom WMI-Dienst erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="38780-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="38780-290">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-291">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM- \| Protokolldatei maximale Größe**</span><span class="sxs-lookup"><span data-stu-id="38780-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="38780-292">**Maxwaitonclientobjects**</span><span class="sxs-lookup"><span data-stu-id="38780-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-293">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-294">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-295">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="38780-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="38780-296">Die Zeitspanne, die ein neu erstelltes Objekt auf die Verwendung durch den Client wartet, bevor es verworfen wird, und es wird ein Fehlerwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38780-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="38780-297">Diese Eigenschaft interagiert mit den Eigenschaften **lowmittloldonclientobjects** und **highmittloldonclientobjects** , um die – langsamer zu drosseln – die Übermittlung von Objekten an Consumer, wenn der Consumer die Objekte zu langsam empfängt.</span><span class="sxs-lookup"><span data-stu-id="38780-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="38780-298">**Maxwaitonevents**</span><span class="sxs-lookup"><span data-stu-id="38780-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-299">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38780-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38780-300">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38780-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38780-301">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="38780-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="38780-302">Die Zeitspanne, für die ein Ereignis an einen Client in die Warteschlange eingereiht wird, bevor es verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="38780-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="38780-303">Diese Eigenschaft interacts0 mit **lowmittloldonevents** und **highmittloldonevents** zur Drosselung – verlangsamt die Übermittlung von Objekten an Consumer, wenn der Consumer die Objekte zu langsam empfängt.</span><span class="sxs-lookup"><span data-stu-id="38780-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="38780-304">Diese Eigenschaft gibt den Registrierungs Wert wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-304">This property reflects the registry value.</span></span>

<span data-ttu-id="38780-305">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max. Wartezeit auf Ereignisse (MS)**    </span><span class="sxs-lookup"><span data-stu-id="38780-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="38780-306">**"Mamaselfinstalldirectory"**</span><span class="sxs-lookup"><span data-stu-id="38780-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-309">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")</span><span class="sxs-lookup"><span data-stu-id="38780-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="38780-310">Verzeichnispfad für Anwendungen, die MOF-Dateien im WMI-Repository installieren.</span><span class="sxs-lookup"><span data-stu-id="38780-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="38780-311">WMI kompiliert automatisch alle MOF-Dateien, die in diesem Verzeichnis abgelegt werden, und verschiebt die MOF-Datei, je nach Erfolg, in ein Unterverzeichnis mit der Bezeichnung "gut" oder "schlecht".</span><span class="sxs-lookup"><span data-stu-id="38780-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="38780-312">Wenn der \# [pragma Auto Wiederherstellen](../wmisdk/pragma-autorecover.md) -Befehl enthalten ist, wird der voll qualifizierte Dateiname der **autorecovermufs** -Liste hinzugefügt, die verwendet wird, wenn WMI das Repository initialisiert oder wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="38780-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="38780-313">In der Liste wird die Reihenfolge bestimmt, in der die Zusammenstellung von-und-</span><span class="sxs-lookup"><span data-stu-id="38780-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="38780-314">Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.</span><span class="sxs-lookup"><span data-stu-id="38780-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="38780-315">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = Installationsverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="38780-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="38780-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="38780-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38780-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38780-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38780-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38780-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38780-319">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="38780-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="38780-320">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="38780-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="38780-321">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="38780-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38780-322">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38780-322">Remarks</span></span>

<span data-ttu-id="38780-323">Die **Win32 \_ wmisetting** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="38780-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="38780-324">Auf einem Computer kann nur eine Instanz dieser Klasse vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="38780-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="38780-325">Das wissen, wie WMI auf einem Computer konfiguriert ist, kann sehr nützlich sein, wenn Sie Skripts debuggen oder Probleme mit dem WMI-Dienst selbst beheben.</span><span class="sxs-lookup"><span data-stu-id="38780-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="38780-326">Beispielsweise werden viele WMI-Skripts unter der Annahme geschrieben, dass root \\ CIMV2 der Standard Namespace auf dem Zielcomputer ist.</span><span class="sxs-lookup"><span data-stu-id="38780-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="38780-327">Daher kann es vorkommen, dass Skript Schreiber, die auf eine Klasse in "root \\ CIMv2" zugreifen müssen, den Namespace oft nicht in den GetObject-Moniker einschließen, wie im folgenden Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="38780-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="38780-328">Wenn root \\ CIMV2 nicht der Standard Namespace auf dem Zielcomputer ist, kann dieses Skript nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="38780-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="38780-329">Um dies zu verhindern, muss der Namespace Stamm \\ CIMV2 im Moniker enthalten sein, wie im folgenden Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="38780-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="38780-330">Wenn sich der Standard Namespace auf dem Zielcomputer von dem Namespace unterscheidet, der von einem Skript angenommen wird, schlägt das Skript fehl.</span><span class="sxs-lookup"><span data-stu-id="38780-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="38780-331">Darüber hinaus wird dem Benutzer die etwas irreführende Fehlermeldung "Ungültige Klasse" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38780-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="38780-332">Der Fehler ist in Wahrheit nicht, weil die Klasse ungültig ist, aber weil die Klasse im Standard Namespace nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="38780-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="38780-333">Dies ist ein schwieriges Problem bei der Problembehandlung, da Sie wahrscheinlich mögliche Probleme mit der-Klasse untersuchen und keine Probleme mit dem Namespace, der (oder in diesem Fall nicht) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="38780-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="38780-334">Sie können die **Win32 \_ wmisetting** -Klasse verwenden, um zu bestimmen, wie WMI auf einem Computer konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="38780-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="38780-335">Konfigurationsdetails wie z. b. der Standard Namespace oder die WMI-Buildnummer können bei der Problembehandlung von Skript Problemen nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="38780-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="38780-336">Diese Einstellungen bieten außerdem wichtige administrative Informationen, wie z. b. wie oder ob WMI-Fehler auf einem Computer protokolliert werden und welche WMI-Anbieter automatisch erneut geladen werden, wenn Sie das WMI-Repository neu erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="38780-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="38780-337">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38780-337">Examples</span></span>

<span data-ttu-id="38780-338">Das Codebeispiel [Ändern von WMI-Einstellungen](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript in der TechNet Gallery verwendet die **Win32 \_ wmisetting** -Klasse, um das WMI-Sicherungs Intervall und den Protokolliergrad zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="38780-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="38780-339">Der [Liste der Standard Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript-Code in der TechNet Gallery verwendet die **Win32 \_ wmisetting** -Klasse zum Abrufen und Anzeigen der aktuellen WMI-Einstellung "Standard Namespace für die Skripterstellung".</span><span class="sxs-lookup"><span data-stu-id="38780-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="38780-340">Das Codebeispiel für das [Ändern des standardmäßigen WMI-Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript in der TechNet Gallery verwendet die **ASPScriptDefaultNamespace** -Eigenschaft, um die WMI-Einstellung "Standard Namespace für die Skripterstellung" auf "root \\ CIMV2" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="38780-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="38780-341">Das Codebeispiel [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBScript verwendet eine Reihe von Eigenschaften für **Win32 \_ wmisetting** , um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="38780-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="38780-342">Im JavaScript-Codebeispiel für das [Auflisten von WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) -Einstellungs Informationen wird eine Reihe von Eigenschaften für **Win32- \_ wmisetting** verwendet, um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="38780-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="38780-343">Im python-Codebeispiel für das [Auflisten von WMI-Einstellungsinformationen](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) wird eine Reihe von Eigenschaften für **Win32 \_ wmisetting** verwendet, um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="38780-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="38780-344">Das Codebeispiel für die [Auflistung von WMI-Einstellungs Informationen](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Objekt REXX verwendet eine Reihe von Eigenschaften für **Win32 \_ wmisetting** , um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="38780-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="38780-345">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie die WMI-Version abrufen, die auf dem lokalen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38780-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="38780-346">"Win32 \_ wmisetting = @" gibt die einzelne Instanz der Klasse an.</span><span class="sxs-lookup"><span data-stu-id="38780-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="38780-347">Weitere Informationen finden Sie unter WMI-Versionen.</span><span class="sxs-lookup"><span data-stu-id="38780-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="38780-348">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38780-348">Requirements</span></span>



| <span data-ttu-id="38780-349">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38780-349">Requirement</span></span> | <span data-ttu-id="38780-350">Wert</span><span class="sxs-lookup"><span data-stu-id="38780-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38780-351">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38780-351">Minimum supported client</span></span><br/> | <span data-ttu-id="38780-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38780-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38780-353">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38780-353">Minimum supported server</span></span><br/> | <span data-ttu-id="38780-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38780-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38780-355">Namespace</span><span class="sxs-lookup"><span data-stu-id="38780-355">Namespace</span></span><br/>                | <span data-ttu-id="38780-356">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="38780-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38780-357">MOF</span><span class="sxs-lookup"><span data-stu-id="38780-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38780-358"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="38780-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38780-359">DLL</span><span class="sxs-lookup"><span data-stu-id="38780-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38780-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38780-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38780-361">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38780-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38780-362">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="38780-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="38780-363">WMI-Dienst Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="38780-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
