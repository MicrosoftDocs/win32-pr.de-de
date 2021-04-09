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
# <a name="win32_startupcommand-class"></a>Win32- \_ startupcommand-Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ startupcommand** stellt einen Befehl dar, der automatisch ausgeführt wird, wenn sich ein Benutzer am Computersystem anmeldet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ startupcommand** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ startupcommand** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Befehl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")
</dt> </dl>

Befehl, der vom Startbefehl ausgeführt wird.

WMI erhält diese Daten aus dem Registrierungsschlüssel.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**

Beispiel: "C: \\ Windows \\notepad.exe myfile.txt"

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

**Location**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Windows")
</dt> </dl>

Der Pfad, in dem sich der Startbefehl auf dem Dateisystem befindet.

Beispiel: HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Start** ("Startup")


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Gemeinsamer Start** ("gemeinsamer Start")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")


</dt> <dd></dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")
</dt> </dl>

Der Dateiname des Start Befehls.

Beispiel: "findfast"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Benutzer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Der Benutzername, für den dieser Startbefehl ausgeführt wird.

Beispiel: "mydomain \\ myname"

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Die UserSID-Eigenschaft gibt die SID des Benutzers an, für den dieser Startbefehl ausgeführt wird. Diese Benutzer Eigenschaft ist möglicherweise leer, aber die UserSID hat weiterhin einen Wert, wenn der Benutzername nicht aufgelöst werden kann (z. b. im Fall eines gelöschten Benutzers). Die-Eigenschaft ist hilfreich, um zwischen den Befehlen zu unterscheiden, die mit nicht aufgelösten, nicht aufgelösten, nicht Dieser Wert kann NULL sein, wenn der Befehl Elementen zugeordnet ist, die einen Benutzer nicht wie alle Benutzer identifizieren.

Beispiel: S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ startupcommand** ist von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

Das Starten des Computers endet nicht, nachdem das Betriebssystem geladen wurde. Stattdessen kann das Windows-Betriebssystem so konfiguriert werden, dass Start Befehle bei jedem Start von Windows ausgeführt werden. Start Befehle werden in der Registrierung oder als Teil des Benutzerprofils gespeichert und zum automatischen Starten angegebener Skripts oder Anwendungen bei jedem Laden von Windows verwendet.

In den meisten Fällen sind Autostart-Programme nützlich. Sie stellen sicher, dass bestimmte Anwendungen, z. b. Antivirussoftware, beim Laden von Fenstern automatisch gestartet und ausgeführt werden. Autostart-Programme können jedoch auch für Probleme verantwortlich sein, z. b.:

-   Computer, deren Start sehr viel Zeit in Anspruch nimmt. Dies kann auf eine große Anzahl von Anwendungen zurückzuführen sein, die bei jedem Start von Windows gestartet werden müssen.
-   Anwendungen, die in der Taskleiste oder im Task-Manager dargestellt werden, auch wenn der Benutzer Sie nicht gestartet hat. Obwohl diese Anwendungen nicht zwangsläufig Probleme verursachen, kann dies dazu führen, dass Helpdeskmitarbeiter von Benutzern, die nicht wissen, woher diese Programme stammen und warum Sie ausgeführt werden, dazu führen können.
-   Computer, die Probleme haben, auch wenn Sie sich im Leerlauf befinden. Diese Probleme sind häufig auf Start Befehle zurückzuführen, die ausgeführt werden, wenn niemand weiß, dass Sie ausgeführt werden.

Das Identifizieren der Anwendungen und Skripts, die beim Start automatisch ausgeführt werden, ist eine wichtige, aber schwierige administrative Aufgabe, da Start Befehle an vielen verschiedenen Speicherorten gespeichert werden können:

-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   System Drive \\ Dokumente und Einstellungen \\ alle Benutzer \\ Start Menü \\ Programme \\ starten
-   System Drive \\ Documents and Settings \\ username \\ Startmenü \\ Programme \\ Startup

Sie können die WMI-Win32- \_ startupcommand-Klasse verwenden, um Autostart-Programme unabhängig davon aufzulisten, wo die Informationen gespeichert werden.

Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen. Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).

Sie können die Registrierungs Werte ändern, wenn **Win32 \_ startupcommand** Daten abruft, indem Sie die Methoden der WMI- [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) in Skripts oder in C++ aufrufen. Weitere Informationen finden Sie unter [Ändern der System Registrierung](../wmisdk/modifying-the-system-registry.md).

## <a name="examples"></a>Beispiele

Das folgende VBScript listet die Start Befehle auf einem Computer auf.


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

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
