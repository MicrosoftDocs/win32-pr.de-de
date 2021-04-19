---
description: Die \_ WMI-Klasse "Win32 bootconfiguration" stellt die Startkonfiguration eines Computer Systems dar, auf dem Windows ausgeführt wird.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Win32_BootConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342778"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="c08ae-103">Win32- \_ bootconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="c08ae-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="c08ae-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ bootconfiguration** " stellt die Startkonfiguration eines Computer Systems dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c08ae-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="c08ae-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c08ae-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c08ae-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c08ae-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08ae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c08ae-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="c08ae-108">Member</span><span class="sxs-lookup"><span data-stu-id="c08ae-108">Members</span></span>

<span data-ttu-id="c08ae-109">Die **Win32- \_ bootconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c08ae-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="c08ae-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c08ae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c08ae-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c08ae-111">Properties</span></span>

<span data-ttu-id="c08ae-112">Die **Win32- \_ bootconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c08ae-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c08ae-113">**BootDirectory**</span><span class="sxs-lookup"><span data-stu-id="c08ae-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-116">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="c08ae-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-117">Der Pfad zu den Systemdateien, die für den Systemstart erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c08ae-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="c08ae-118">Beispiel: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="c08ae-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c08ae-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c08ae-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-123">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c08ae-123">Short textual description of the current object.</span></span>

<span data-ttu-id="c08ae-124">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c08ae-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="c08ae-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="c08ae-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-129">Pfad zu den Konfigurationsdateien.</span><span class="sxs-lookup"><span data-stu-id="c08ae-129">Path to the configuration files.</span></span> <span data-ttu-id="c08ae-130">Dieser Wert ähnelt möglicherweise dem Wert in der **BootDirectory** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c08ae-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c08ae-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-134">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c08ae-134">Textual description of the current object.</span></span>

<span data-ttu-id="c08ae-135">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c08ae-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-136">**Lastdrive**</span><span class="sxs-lookup"><span data-stu-id="c08ae-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="c08ae-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-140">Der letzte Laufwerk Buchstabe, dem ein physisches Laufwerk zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c08ae-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="c08ae-141">Beispiel: "E:"</span><span class="sxs-lookup"><span data-stu-id="c08ae-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="c08ae-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-145">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c08ae-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-146">Der Name der Startkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c08ae-146">Name of the boot configuration.</span></span> <span data-ttu-id="c08ae-147">Es handelt sich um einen Bezeichner für die Startkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c08ae-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-148">**ScratchDirectory**</span><span class="sxs-lookup"><span data-stu-id="c08ae-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-151">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="c08ae-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-152">Verzeichnis, in dem sich temporäre Dateien während der Startzeit befinden können.</span><span class="sxs-lookup"><span data-stu-id="c08ae-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="c08ae-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-156">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c08ae-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-157">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c08ae-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="c08ae-158">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c08ae-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c08ae-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="c08ae-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ae-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c08ae-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c08ae-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ae-162">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="c08ae-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="c08ae-163">Verzeichnis, in dem temporäre Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c08ae-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="c08ae-164">Beispiel: "C: \\ Temp"</span><span class="sxs-lookup"><span data-stu-id="c08ae-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c08ae-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c08ae-165">Remarks</span></span>

<span data-ttu-id="c08ae-166">Die **Win32- \_ bootconfiguration** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c08ae-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c08ae-167">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c08ae-167">Examples</span></span>

<span data-ttu-id="c08ae-168">Im Beispiel [Auflisten der Start Konfigurations Eigenschaften eines Computers](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) perl werden Start Konfigurationsinformationen für einen Computer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c08ae-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="c08ae-169">Im folgenden VBScript-Beispiel werden Start Konfigurationsinformationen für einen Computer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c08ae-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="c08ae-170">Im folgenden Codebeispiel wird die Verwendung der WMI-Klasse für die **Win32- \_ bootconfiguration** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c08ae-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="c08ae-171">Im vorherigen Codebeispiel wird die folgende Ausgabe erstellt:</span><span class="sxs-lookup"><span data-stu-id="c08ae-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="c08ae-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c08ae-172">Requirements</span></span>



| <span data-ttu-id="c08ae-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c08ae-173">Requirement</span></span> | <span data-ttu-id="c08ae-174">Wert</span><span class="sxs-lookup"><span data-stu-id="c08ae-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c08ae-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c08ae-175">Minimum supported client</span></span><br/> | <span data-ttu-id="c08ae-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c08ae-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c08ae-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c08ae-177">Minimum supported server</span></span><br/> | <span data-ttu-id="c08ae-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c08ae-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c08ae-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="c08ae-179">Namespace</span></span><br/>                | <span data-ttu-id="c08ae-180">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c08ae-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c08ae-181">MOF</span><span class="sxs-lookup"><span data-stu-id="c08ae-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c08ae-182"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c08ae-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c08ae-183">DLL</span><span class="sxs-lookup"><span data-stu-id="c08ae-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c08ae-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c08ae-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08ae-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c08ae-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08ae-186">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="c08ae-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="c08ae-187">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c08ae-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

