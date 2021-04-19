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
# <a name="win32_bootconfiguration-class"></a>Win32- \_ bootconfiguration-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ bootconfiguration** " stellt die Startkonfiguration eines Computer Systems dar, auf dem Windows ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32- \_ bootconfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ bootconfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**BootDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")
</dt> </dl>

Der Pfad zu den Systemdateien, die für den Systemstart erforderlich sind.

Beispiel: "C: \\ Windows"

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**ConfigurationPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")
</dt> </dl>

Pfad zu den Konfigurationsdateien. Dieser Wert ähnelt möglicherweise dem Wert in der **BootDirectory** -Eigenschaft.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Lastdrive**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetDriveType")
</dt> </dl>

Der letzte Laufwerk Buchstabe, dem ein physisches Laufwerk zugewiesen wird.

Beispiel: "E:"

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Der Name der Startkonfiguration. Es handelt sich um einen Bezeichner für die Startkonfiguration.

</dd> <dt>

**ScratchDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetTempPath")
</dt> </dl>

Verzeichnis, in dem sich temporäre Dateien während der Startzeit befinden können.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**TempDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetTempPath")
</dt> </dl>

Verzeichnis, in dem temporäre Dateien gespeichert werden.

Beispiel: "C: \\ Temp"

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ bootconfiguration** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

## <a name="examples"></a>Beispiele

Im Beispiel [Auflisten der Start Konfigurations Eigenschaften eines Computers](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) perl werden Start Konfigurationsinformationen für einen Computer zurückgegeben.

Im folgenden VBScript-Beispiel werden Start Konfigurationsinformationen für einen Computer zurückgegeben.


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



Im folgenden Codebeispiel wird die Verwendung der WMI-Klasse für die **Win32- \_ bootconfiguration** veranschaulicht.


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



Im vorherigen Codebeispiel wird die folgende Ausgabe erstellt:

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

