---
description: Die Win32 \_ desktopwmi-Klasse stellt die allgemeinen Merkmale des Desktops eines Benutzers dar. Die Eigenschaften dieser Klasse können vom Benutzer geändert werden, um den Desktop anzupassen.
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
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861719"
---
# <a name="win32_desktop-class"></a>Win32 \_ -Desktop Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für den **Win32 \_ -Desktop** stellt die allgemeinen Merkmale des Desktops eines Benutzers dar. Die Eigenschaften dieser Klasse können vom Benutzer geändert werden, um den Desktop anzupassen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32 \_ -Desktop** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ -Desktop** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Rahmenbreite**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ")
</dt> </dl>

Breite der Rahmen um alle Fenster mit anpassbaren Rändern.

Beispiel: 3

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

**Coolswitch**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop \| coolswitch")
</dt> </dl>

Der schnelle Aufgaben Wechsel ist aktiviert. Der schnelle Aufgaben Wechsel ermöglicht es dem Benutzer, mithilfe der Tastenkombination **Alt + Tab** zwischen Fenstern zu wechseln.

</dd> <dt>

**Cursor-Blinkrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop \| geschweisorblinkrate"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")
</dt> </dl>

Zeitspanne zwischen aufeinander folgenden Cursor-Blinks.

Beispiel: 530

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

**DragFullWindows**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop \| DragFullWindows")
</dt> </dl>

Der Inhalt eines Fensters wird angezeigt, wenn ein Benutzer das Fenster verschiebt.

</dd> <dt>

**Gridgranularität**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop- \| Granularität"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Pixel")
</dt> </dl>

Abstand des Rasters, an das Windows auf dem Desktop gebunden ist. Dies erleichtert das Organisieren von Fenstern. Der Abstand ist in der Regel ausreichend, dass der Benutzer ihn nicht bemerkt.

Beispiel: 1

</dd> <dt>

**IconSpacing**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")
</dt> </dl>

Abstand zwischen Symbolen.

Beispiel: 75

</dd> <dt>

**Icontitlefakename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ")
</dt> </dl>

Schriftart, die für die Namen der Symbole verwendet wird.

Beispiel: "MS San Serif"

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**logfontw**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfheight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")
</dt> </dl>

Schriftart Größe des Symbols.

Beispiel: 9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ")
</dt> </dl>

Der Titeltext des Symbols wird in die nächste Zeile umschlossen.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Der Name, der das aktuelle Desktop Profil identifiziert.

Beispiel: "mainprof"

</dd> <dt>

**Muster**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -System Steuerungs \\ \\ Desktop- \| Muster ")
</dt> </dl>

Der Name des Musters, das als Hintergrund für den Desktop verwendet wird.

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \| screensaveactive ")
</dt> </dl>

Der Bildschirmschoner ist aktiv.

</dd> <dt>

**Screensaverausführ Bare Datei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \|SCRNSAVE.EXE ")
</dt> </dl>

Der Name der aktuellen ausführbaren Datei für den Bildschirmschoner.

Beispiel: "Login. SCR

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \| ScreenSaverIsSecure ")
</dt> </dl>

Das Kennwort ist für den Bildschirmschoner aktiviert.

</dd> <dt>

**Screensavertimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \| SCREENSAVETIMEOUT "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Sekunden ")
</dt> </dl>

Die Zeitspanne, die vor dem Start des Bildschirmschoners verstrichen ist.

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

**Hintergrundbild**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -System Steuerungs \\ \\ Desktop- \| Hintergrundbild ")
</dt> </dl>

Der Dateiname für das Hintergrundbild im Hintergrund des Desktops.

Beispiel: "WINNT.BMP"

</dd> <dt>

**Wallpapier gestreckt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \| Wallart ")
</dt> </dl>

Das Hintergrundbild wird gestreckt, um den gesamten Bildschirm auszufüllen. Microsoft Plus! muss installiert werden, bevor diese Option verfügbar ist. Wenn der Wert **false** ist, behält das Hintergrund seine ursprünglichen Dimensionen im Desktop Hintergrund.

</dd> <dt>

**Wallpapierkachel**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \| tilewallpaper ")
</dt> </dl>

Das Hintergrundbild wird gekachelt oder zentriert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ -Desktop** Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen. Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird das Abrufen von Desktop Informationen beschrieben.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

