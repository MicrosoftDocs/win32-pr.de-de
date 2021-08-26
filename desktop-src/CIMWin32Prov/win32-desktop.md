---
description: Die Win32 \_ DesktopWMI-Klasse stellt die allgemeinen Merkmale des Desktops eines Benutzers dar. Die Eigenschaften dieser Klasse können vom Benutzer geändert werden, um den Desktop anzupassen.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c59adebd2fdf3c0727016473e6c347be3af139d539bb007c794eb2aafb4c1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002880"
---
# <a name="win32_desktop-class"></a>Win32 \_ Desktop-Klasse

Die **Win32 \_ Desktop**[WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die allgemeinen Merkmale des Desktops eines Benutzers dar. Die Eigenschaften dieser Klasse können vom Benutzer geändert werden, um den Desktop anzupassen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>Member

Die **Win32 \_ Desktop-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Desktop-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Rahmenbreite**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung Desktop \\ \\ \\ \\ WindowMetrics \| BorderWidth")
</dt> </dl>

Breite der Rahmen um alle Fenster mit anpassbaren Rahmen.

Beispiel: 3

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**CoolSwitch**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Systemsteuerung Desktop \\ \\ \| CoolSwitch")
</dt> </dl>

Schnelles Wechseln von Aufgaben ist aktiviert. Schnelles Wechseln von Aufgaben ermöglicht es dem Benutzer, mithilfe der Tastenkombination **ALT+TAB** zwischen Fenstern zu wechseln.

</dd> <dt>

**CursorBlinkRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Systemsteuerung Desktop \\ \\ \| CursorBlinkRate"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")
</dt> </dl>

Die Zeitspanne zwischen aufeinanderfolgenden Cursorblinzeln.

Beispiel: 530

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**DragFullWindows**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Systemsteuerung Desktop \\ \\ \| DragFullWindows")
</dt> </dl>

Der Inhalt eines Fensters wird angezeigt, wenn ein Benutzer das Fenster verschiebt.

</dd> <dt>

**GridGranularity**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Systemsteuerung Desktop \\ \\ \| GridGranularity"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Pixel")
</dt> </dl>

Abstand des Rasters, an das Fenster auf dem Desktop gebunden sind. Dies erleichtert das Organisieren von Fenstern. Der Abstand ist in der Regel ausreichend, damit der Benutzer ihn nicht bemerkt.

Beispiel: 1

</dd> <dt>

**SymbolSpacing**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ \\ \\ DesktopfensterMetrikensymbolSpacing"), \| [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")
</dt> </dl>

Abstand zwischen Symbolen.

Beispiel: 75

</dd> <dt>

**IconTitleFaceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ Desktop \\ \\ WindowMetrics \| IconFont")
</dt> </dl>

Schriftart, die für die Namen der Symbole verwendet wird.

Beispiel: "MS San Serif"

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")
</dt> </dl>

Schriftgrad des Symbols.

Beispiel: 9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap")
</dt> </dl>

Der Titeltext des Symbols wird in die nächste Zeile umbrochen.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Name, der das aktuelle Desktopprofil identifiziert.

Beispiel: "MainProf"

</dd> <dt>

**Muster**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ \| DesktopMuster")
</dt> </dl>

Name des Musters, das als Hintergrund für den Desktop verwendet wird.

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung Desktop \\ \\ \| ScreenSaveActive")
</dt> </dl>

Bildschirmschoner ist aktiv.

</dd> <dt>

**ScreenSaverExecutable**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ Desktop \|SCRNSAVE.EXE")
</dt> </dl>

Name der ausführbaren Datei des aktuellen Bildschirmschonrs.

Beispiel: "LOGON. SCR"

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung Desktop \\ \\ \| ScreenSaverIsSecure")
</dt> </dl>

Das Kennwort ist für den Bildschirmschoner aktiviert.

</dd> <dt>

**ScreenSaverTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ Desktop \| ScreenSaveTimeOut"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")
</dt> </dl>

Die Zeitspanne, die verstreicht, bevor der Bildschirmschoner gestartet wird.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Bezeichner, durch den das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**Hintergrundbild**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung Desktop \\ \\ \| Wallpaper")
</dt> </dl>

Dateiname für das Hintergrundbilddesign im Hintergrund des Desktops.

Beispiel: "WINNT.BMP"

</dd> <dt>

**WallpaperStretched**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung Desktop \\ \\ \| WallpaperStyle")
</dt> </dl>

Hintergrundbild wird gestreckt, um den gesamten Bildschirm zu füllen. Microsoft Plus! muss installiert sein, bevor diese Option verfügbar ist. **False** gibt an, dass das Hintergrundbild seine ursprünglichen Abmessungen auf dem Desktophintergrund beibehält.

</dd> <dt>

**WallpaperTiled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Systemsteuerung \\ \\ Desktop \| TileWallpaper")
</dt> </dl>

Hintergrundbilder sind gekachelt oder zentriert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ Desktop-Klasse** wird von [**der \_ CIM-Einstellung**](cim-setting.md)abgeleitet.

Der aufrufende Prozess, der diese Klasse verwendet, muss über die **SE \_ RESTORE \_ NAME-Berechtigung** auf dem Computer verfügen, auf dem sich die Registrierung befindet. Wenn Sie diese Klasse beispielsweise auf dem lokalen Computer aufzählen, muss das Konto, unter dem die Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge.](/windows/desktop/WmiSdk/executing-privileged-operations)

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird beschrieben, wie Desktopinformationen abgerufen werden.


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

