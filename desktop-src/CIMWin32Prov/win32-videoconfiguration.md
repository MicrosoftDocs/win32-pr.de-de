---
description: Die Win32 \_ VideoConfiguration-Klasse ist nicht aktiv. Es werden keine Instanzen zurückgegeben, da kein Anbieter sie unterstützt.
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
ms.openlocfilehash: 7d951a8927458fa12398682ce63963dd71949d70e4db3a426dfc93ad14c78bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922620"
---
# <a name="win32_videoconfiguration-class"></a>Win32 \_ VideoConfiguration-Klasse

Die **Win32 \_ VideoConfiguration-Klasse** ist nicht aktiv. Es werden keine Instanzen zurückgegeben, da kein Anbieter sie unterstützt.

Die **Win32 \_ VideoConfiguration-Klasse** stellt eine Konfiguration eines Videosubsystems dar. Diese Klasse wurde zugunsten der Eigenschaften in den Klassen [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)und [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) als veraltet eingestuft.

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

Die **Win32 \_ VideoConfiguration-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ VideoConfiguration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Gerätekontextfunktionen \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Pixel")
</dt> </dl>

Gibt die aktuelle Farbtiefe der Videoanzeige an.

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ \\ \\ Services-Klasse \\ \\ Info \| ChipType")
</dt> </dl>

Enthält den Namen des Adapterchips.

Beispiel: s3

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**AdapterKompatibilität**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**Schlüssel,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt den Namen des Herstellers des Adapters an. Dieser Name kann verwendet werden, um die Kompatibilität dieses Geräts mit den Anforderungen des Computersystems zu vergleichen.

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ \\ \\ Services-Klasse \\ \\ Info \| DACType")
</dt> </dl>

Gibt den Namen des digital-to-analog-Chips (DAC) an, der im Adapter verwendet wird.

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Enthält eine Beschreibung oder einen beschreibenden Namen der Grafikkarte.

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ Info \\ \\ \| VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Gibt die Arbeitsspeichergröße der Grafikkarte an.

Beispiel: 16777216

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HARDWARE Description System \\ \\ \\ \\ \\ \\ DisplayController \\ \\ 0 \\ \\ Identifier")
</dt> </dl>

Gibt den Typ der Grafikkarte an.

Zeichensatz: Alphanumerisch

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Gerätekontextfunktionen \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

Gibt die tatsächliche Anzahl von Bits pro Pixel an, die die Anzeige darstellen. Dies kann auf die aktuelle Videoeinstellung (dargestellt durch die ActualColorResolution-Eigenschaft) des Benutzers skaliert werden.

Beispiel: 8

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Gerätekontextfunktionen \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| PLANES")
</dt> </dl>

Gibt die aktuelle Anzahl von Farbebenen an, die in der Videoanzeige verwendet werden. Eine Farbebene ist eine weitere Möglichkeit, Pixelfarben darzustellen. Anstatt jedem Pixel einen einzelnen RGB-Wert zuzuweisen, trennen Farbebenen die Grafik in jede der primären Farbkomponenten (Rotgrünblau) und speichern sie in ihren eigenen Ebenen. Dies ermöglicht größere Farbtiefe auf 8- und 16-Bit-Videosystemen. Bei vorhandenen Grafiksystemen ist die Bitbreite groß genug, um Farbtiefeinformationen zu speichern, sodass nur eine Farbebene erforderlich ist.

Beispiel: 1

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Gerätekontextfunktionen \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Gibt die Anzahl der Farbindizes in einer Farbtabelle für eine Videoanzeige an. Diese Eigenschaft wird verwendet, wenn das Gerät eine Farbtiefe von maximal 8 Bits pro Pixel aufweist. Für Geräte mit höheren Farbtiefe wird -1 zurückgegeben.

Beispiel: 256

Diese Eigenschaft wurde zugunsten der entsprechenden Eigenschaften, die in [**Win32 \_ VideoController, Win32**](win32-videocontroller.md) [**\_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)enthalten sind, als veraltet bezeichnet.

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

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Gibt die aktuelle Anzahl gerätespezifischer Stifte an. Der Wert 0xFFFFFFFF bedeutet, dass das Gerät keine Stifte unterstützt. Stifte werden verwendet, um Linien und die Reihenfolgen polygonaler Objekte zu zeichnen.

Beispiel: 3

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry-System \| \\ \\ CurrentControlSet \\ \\ \\ \\ \\ \\ Services-KlassenadapterDescription \| DriverDate")
</dt> </dl>

Gibt das Datum und die Uhrzeit der Installation des aktuellen Videotreibers an.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")
</dt> </dl>

Gibt die aktuelle Anzahl von Pixeln in horizontaler Richtung (X-Achse) der Anzeige an.

Beispiel: 1024

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \| InfPath")
</dt> </dl>

Gibt den Pfad zur INF-Datei des Videotreibers an.

Beispiel: C: \\ Windows \\ System32-Treiber \\

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \| InfSection")
</dt> </dl>

Gibt den Abschnitt der INF-Datei an, in dem sich die Win32-Videoinformationen befinden.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Defaule \| drv")
</dt> </dl>

Gibt den Namen des installierten Videotreibers an.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**MonitorManufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt den Namen des Herstellers des Anzeigegeräts an.

Beispiel: NEC

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**MonitorType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HARDWARE Description System \\ \\ \\ \\ \\ \\ MonitorPeripheral \\ \\ 0 \| Identifier")
</dt> </dl>

Gibt den Modellnamen des Anzeigegeräts an.

Beispiel: NEC 5FGp

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**Schlüssel,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Enthält einen identifizierenden Namen für die Videokonfigurationsklasse.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**PixelsPerXLogicalInch**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")
</dt> </dl>

Gibt die Anzahl der Pixel pro logischem Zoll entlang der X-Achse (horizontale Richtung) der Anzeige an.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**PixelsPerYLogicalInch**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")
</dt> </dl>

Gibt die Anzahl von Pixeln pro logischem Zoll entlang der Y-Achse (vertikale Richtung) der Anzeige an.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")
</dt> </dl>

Gibt die Aktualisierungsrate der Videokonfiguration an. Der Wert 0 oder 1 gibt an, dass eine Standardrate verwendet wird.

Beispiel: 72

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings.Interlaced")
</dt> </dl>

Gibt an, ob das Anzeigegerät geschachtelt ist.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**Nicht-Interlaced** ("Non Interlaced")


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

**Interlaced** ("Interlaced")


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Gerätekontextfunktionen \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millimeter")
</dt> </dl>

Gibt die Höhe des physischen Bildschirms an.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Gerätekontextfunktionen \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millimeter")
</dt> </dl>

Gibt die Breite des physischen Bildschirms an.

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, unter dem das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")
</dt> </dl>

Bezeichnet die aktuelle Anzahl von Farbindexeinträgen, die für die Systemnutzung reserviert sind. Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden. Indizierte Paletten werden nicht für Farbtiefen von mehr als 8 Bits pro Pixel verwendet. Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **NULL festgelegt.**

Beispiel: 20

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")
</dt> </dl>

Gibt die aktuelle Anzahl von Pixeln in vertikaler Richtung (Y-Achse) der Anzeige an.

Beispiel: 768

Diese Eigenschaft wurde zugunsten einer entsprechenden Eigenschaft veraltet, die in [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) und/oder [**CIM \_ VideoControllerResolution enthalten ist.**](cim-videocontrollerresolution.md)

</dd> </dl>

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
</dt> </dl>

 

 
