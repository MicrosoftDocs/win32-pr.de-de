---
description: Die Win32 \_ displaycontrollerconfiguration-WMI-Klasse stellt die Grafikkarten-Konfigurationsinformationen eines Computer Systems dar, auf dem Windows ausgeführt wird.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Win32_DisplayControllerConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127336"
---
# <a name="win32_displaycontrollerconfiguration-class"></a>Win32 \_ displaycontrollerconfiguration-Klasse

Die **Win32 \_ displaycontrollerconfiguration** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Grafikkarten-Konfigurationsinformationen eines Computer Systems dar, auf dem Windows ausgeführt wird.

Diese Klasse ist veraltet. Anstelle dieser Klasse sollten Sie die Eigenschaften in den Klassen [**Win32 \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)und [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) verwenden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a>Member

Die **Win32-Klasse \_ displaycontrollerconfiguration** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32-Klasse \_ displaycontrollerconfiguration** verfügt über diese Eigenschaften.

<dl> <dt>

**Bitsper Pixel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| bitspixel")
</dt> </dl>

Entweder die Anzahl der Bits, die zur Darstellung der Farbe in dieser Konfiguration verwendet werden, oder die Bits in jedem Pixel.

Beispiel: 8

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

**Colorplane**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| Plane")
</dt> </dl>

Aktuelle Anzahl von Farbebenen, die in der Anzeige Konfiguration verwendet werden. Eine Farb Ebene ist eine andere Möglichkeit zur Darstellung von Pixel Farben. Anstatt jedem Pixel einen einzelnen RGB-Wert zuzuweisen, trennen Farbebenen die Grafik in jede der primären Farbkomponenten (rot, grün, blau) und speichern Sie in ihren eigenen Ebenen. Dies ermöglicht eine höhere Farbtiefe auf 8-Bit-und 16-Bit-Videosystemen. Vorhandene Grafik Systeme verfügen über den bitwidth, der groß genug ist, um Detailinformationen zu speichern, was bedeutet, dass nur eine Farbebene erforderlich ist.

Beispiel: 1

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

**DeviceEntriesInAColorTable**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numcolors")
</dt> </dl>

Anzahl der Farbindizes in einer Farbtabelle eines Anzeige Geräts (wenn das Gerät eine Farbtiefe von höchstens 8 Bits pro Pixel aufweist). Bei Geräten mit größerer Farbtiefe wird-1 zurückgegeben.

Beispiel: 256

</dd> <dt>

**Geräte Einstellungs Stifte**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numpens")
</dt> </dl>

Aktuelle Anzahl der gerätespezifischen Stifte. Der Wert 0xFFFFFFFF bedeutet, dass das Gerät keine Stifte unterstützt. Stifte sind logische Eigenschaften, die vom Anzeige Controller zum Anzeigen von Geräten zugewiesen werden können und zum Zeichnen von Linien, Rahmen von Polygonen und Text verwendet werden.

Beispiel: 3

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| horzres"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")
</dt> </dl>

Aktuelle Anzahl der Pixel in der horizontalen Richtung (x-Achse) der Anzeige.

Beispiel: 1024

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Der Name des Adapters, der in dieser Konfiguration verwendet wird.

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| horzresvrefresh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")
</dt> </dl>

Aktualisierungsrate der Grafikkarte. Der Wert 0 (null) oder 1 (eins) gibt an, dass ein Standardsatz verwendet wird. Der Wert-1 gibt an, dass eine optimale Rate verwendet wird.

Beispiel: 72

</dd> <dt>

**ReservedSystemPaletteEntries**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numreserved")
</dt> </dl>

Aktuelle Anzahl der Farb Indexeinträge, die für die System Verwendung reserviert sind. Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden. Indizierte Paletten werden nicht für Farbtiefe verwendet, die größer als 8 Bits pro Pixel ist. Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **null** festgelegt.

Beispiel: 20

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

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numreserved")
</dt> </dl>

Aktuelle Anzahl der Farb Indexeinträge, die für die System Verwendung reserviert sind. Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden. Indizierte Paletten werden nicht für Farbtiefe verwendet, die größer als 8 Bits pro Pixel ist. Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **null** festgelegt.

Beispiel: 20

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| vertres"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")
</dt> </dl>

Aktuelle Anzahl der Pixel in vertikaler Richtung (y-Achse) der Anzeige.

Beispiel: 768

</dd> <dt>

**Videomode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Benutzer lesbare Beschreibung der aktuellen Bildschirmauflösung und der Farbeinstellung der Anzeige.

Beispiel: "1024 768 mit 256 Farben"

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ displaycontrollerconfiguration** wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

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

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

