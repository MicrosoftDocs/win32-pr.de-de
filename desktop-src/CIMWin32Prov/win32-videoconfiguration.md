---
description: Die Win32- \_ videoconfiguration-Klasse ist nicht aktiv. Es werden keine Instanzen zurückgegeben, da es von keinem Anbieter unterstützt wird.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523195"
---
# <a name="win32_videoconfiguration-class"></a>Win32- \_ videoconfiguration-Klasse

Die **Win32- \_ videoconfiguration** -Klasse ist nicht aktiv. Es werden keine Instanzen zurückgegeben, da es von keinem Anbieter unterstützt wird.

Die **Win32- \_ videoconfiguration** -Klasse stellt eine Konfiguration eines Video Subsystems dar. Diese Klasse ist zugunsten der Eigenschaften in den [**Win32- \_ Videocontroller**](win32-videocontroller.md)-, [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)-und [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klassen veraltet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Member

Die **Win32- \_ videoconfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ videoconfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| colorres"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Pixel")
</dt> </dl>

Gibt die aktuelle Farbtiefe der Videoanzeige an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| chiptype")
</dt> </dl>

Enthält den Namen des Adapter Chips.

Beispiel: S3

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt den Namen des Herstellers des Adapters an. Dieser Name kann verwendet werden, um die Kompatibilität dieses Geräts mit den Anforderungen des Computer Systems zu vergleichen.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| dactype")
</dt> </dl>

Gibt den Namen des im Adapter verwendeten Digital-to-Analog-Chips (DAC) an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Enthält eine Beschreibung oder einen beschreibenden Namen der Grafikkarte.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| videomemory"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Gibt die Arbeitsspeicher Größe der Grafikkarte an.

Beispiel: 16777216

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \\ \\ Display Controller \\ \\ 0 \\ \\ Identifier")
</dt> </dl>

Gibt den Typ der Grafikkarte an.

Zeichensatz: Alphanumerisch

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Bitsper Pixel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| bitspixel")
</dt> </dl>

Gibt die tatsächliche Anzahl von Bits pro Pixel an, die die Anzeige darstellt. Dies kann auf die aktuelle Video Einstellung (dargestellt durch die ActualColorResolution-Eigenschaft) des Benutzers skaliert werden.

Beispiel: 8

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

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

**Colorplane**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| Plane")
</dt> </dl>

Gibt die aktuelle Anzahl von Farbebenen an, die in der Videoanzeige verwendet werden. Eine Farb Ebene ist eine andere Möglichkeit zur Darstellung von Pixel Farben. Anstatt jedem Pixel einen einzelnen RGB-Wert zuzuweisen, trennen Farbebenen die Grafik in jede der primären Farbkomponenten (rotes grünes blau) und speichern Sie in ihren eigenen Flächen. Dies ermöglicht eine höhere Farbtiefe auf 8-und 16-Bit-Videosystemen. Vorhandene Grafik Systeme verfügen über den bitwidth, der groß genug ist, um farbausführungsinformationen zu speichern, sodass nur eine Farb Ebene erforderlich ist.

Beispiel: 1

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| numcolors")
</dt> </dl>

Gibt die Anzahl der Farbindizes in einer Farbtabelle für eine Videoanzeige an. Diese Eigenschaft wird verwendet, wenn das Gerät über eine Farbtiefe von höchstens 8 Bits pro Pixel verfügt. Bei Geräten mit größerer Farbtiefe wird-1 zurückgegeben.

Beispiel: 256

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

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

**Geräte Einstellungs Stifte**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| numpens")
</dt> </dl>

Gibt die aktuelle Anzahl von gerätespezifischen Stiften an. Der Wert 0xFFFFFFFF bedeutet, dass das Gerät keine Stifte unterstützt. Stifte werden zum Zeichnen von Linien und Rändern von polygonalen Objekten verwendet.

Beispiel: 3

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Driverdate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| driverdate")
</dt> </dl>

Gibt das Datum und die Uhrzeit an, zu der der aktuelle Videotreiber installiert wurde.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| horzres")
</dt> </dl>

Gibt die aktuelle Anzahl der Pixel in der horizontalen Richtung (X-Achse) der Anzeige an.

Beispiel: 1024

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**INFFILENAME**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| INFPath")
</dt> </dl>

Gibt den Pfad zur INF-Datei des Video Treibers an.

Beispiel: C: \\ Windows \\ system32 \\ Drivers

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")
</dt> </dl>

Gibt den Abschnitt der INF-Datei an, in der sich die Win32-Videoinformationen befinden.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ defaule \| drv")
</dt> </dl>

Gibt den Namen des installierten Video Treibers an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Monitorhersteller**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt den Namen des Herstellers des Anzeige Geräts an.

Beispiel: NEC

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Monitortyp**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \\ \\ monitorperipherie \\ \\ 0 \| Identifier")
</dt> </dl>

Gibt den Modellnamen des Anzeige Geräts an.

Beispiel: NEC 5F-GP

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Enthält einen identifizierenden Namen für die Video Konfigurationsklasse.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Pixelsperxlogicalzoll**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| logpixelsx")
</dt> </dl>

Gibt die Anzahl der Pixel pro logischem Zoll entlang der X-Achse (horizontale Richtung) der Anzeige an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Pixelsperylogicalzoll**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| logpixelsy")
</dt> </dl>

Gibt die Anzahl der Pixel pro logischem Zoll entlang der Y-Achse (vertikale Richtung) der Anzeige an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VRefresh")
</dt> </dl>

Gibt die Aktualisierungsrate der Video Konfiguration an. Der Wert 0 oder 1 gibt an, dass ein Standardsatz verwendet wird.

Beispiel: 72

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Scanmode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. interschnür")
</dt> </dl>

Gibt an, ob das Anzeigegerät mit Zeilen Sprung verbunden ist.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**Nicht** Zeilen Sprung ("nicht Zeilen Sprung")


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

Zeilen **Sprung ("** Zeilen Sprung")


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| vertsize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millimeter")
</dt> </dl>

Gibt die Höhe des physischen Bildschirms an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**Bildschirmbreite**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| horzsize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millimeter")
</dt> </dl>

Gibt die Breite des physischen Bildschirms an.

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

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

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")
</dt> </dl>

Gibt die aktuelle Anzahl von Farb Indexeinträgen an, die für die Verwendung durch das System reserviert sind. Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden. Indizierte Paletten werden nicht für Farbtiefe verwendet, die größer als 8 Bits pro Pixel ist. Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **null** festgelegt.

Beispiel: 20

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| vertres")
</dt> </dl>

Gibt die aktuelle Anzahl der Pixel in vertikaler Richtung (Y-Achse) der Anzeige an.

Beispiel: 768

Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.

</dd> </dl>

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
</dt> </dl>

 

 
