---
description: Die \_ WMI-Klasse "Win32 printerconfiguration" stellt die Konfiguration für ein Druckergerät dar. Dies umfasst Funktionen wie Auflösung, Farbe, Schriftarten und Ausrichtung.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Win32_PrinterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958509"
---
# <a name="win32_printerconfiguration-class"></a>Win32- \_ Klasse "printerconfiguration"

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ printerconfiguration** " stellt die Konfiguration für ein Druckergerät dar. Dies umfasst Funktionen wie Auflösung, Farbe, Schriftarten und Ausrichtung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>Member

Die **Win32-Klasse \_ printerconfiguration** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32-Klasse \_ printerconfiguration** verfügt über diese Eigenschaften.

<dl> <dt>

**BitsPerPel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Anzahl von Bits, die zur Darstellung der Farbe in dieser Konfiguration verwendet werden (Bits pro Pixel). Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die Eigenschaften in den [**Win32 \_ Videocontroller**](win32-videocontroller.md)-, [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)-oder [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klassen, um zu bestimmen, wie Farbe dargestellt wird.

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

**Sortieren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die gedruckten Seiten sortiert werden sollen. Zum Sortieren muss das gesamte Dokument gedruckt werden, bevor die nächste Kopie gedruckt wird, anstatt jede Seite des Dokuments so oft wie erforderlich auszugeben.

Diese Eigenschaft wird ignoriert, es sei denn, der Druckertreiber gibt Unterstützung für die Sortierung an.

</dd> <dt>

**Farbe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Farbe des Dokuments. Einige Farbdrucker können mit true Black und nicht mit einer Kombination aus Cyan, Magenta und gelb (CMY) gedruckt werden. Dies erzeugt in der Regel einen dunkleren und stärkeren Text für Dokumente. Diese Option ist nur bei Farbdruckern nützlich, die das echte schwarze Drucken unterstützen.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Monochrom (true schwarz)

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Color

</dd> </dl>

</dd> <dt>

**Exemplare**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der zu druckenden Kopien. Der Druckertreiber muss das Drucken von mehrseitigen Kopien unterstützen.

Beispiel: 2

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

**DeviceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzeige Name des Druckers. Dieser Name ist für den Druckertyp eindeutig und kann aufgrund der Einschränkungen der Zeichenfolge, von der er abgeleitet ist, abgeschnitten werden.

Beispiel: "PCL/HP LaserJet"

</dd> <dt>

**DisplayFlags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Anzeigegerät Farb-oder monochrome ist und ob der Typ der Überprüfung nicht Zeilen Sprung oder Zeilen Sprung ist. Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen Anzeigeeigenschaften, z. b. die **DisplayType** -Eigenschaft der **Win32 \_ Desktopmonitor** -Klasse.

</dd> <dt>

**Display Frequency**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeigt die vertikale Aktualisierungsrate an. Die Aktualisierungsrate für einen Monitor gibt an, wie oft der Bildschirm pro Sekunde neu gezeichnet wird (Häufigkeit). Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die Eigenschaften in der [**Win32 \_ Videocontroller**](win32-videocontroller.md)-, [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)-oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klasse.

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des Druckers. Für diese Eigenschaft können vordefinierte Werte von 1 bis 5 oder Treiber definierte Werte von 6 bis 256 angenommen werden. Linienart-Dithering ist eine spezielle Dithering-Methode, die gut definierte Rahmen zwischen Schwarzen, weißen und grauen Skalierungen erzeugt. Sie eignet sich nicht für Images, die kontinuierliche Abschlüsse in Intensität und Farbton enthalten, wie z. b. gescannte Fotos.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Keine Dithering

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Grober Pinsel

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Feiner Pinsel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Linienart

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5@@**


</dt> <dd>

Grayscale

</dd> </dl>

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Versionsnummer des Windows-basierten Druckertreibers. Die Versionsnummern werden vom Treiber Hersteller erstellt und verwaltet.

</dd> <dt>

**Duplex**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Druckvorgang auf beiden Seiten erfolgt. **False** gibt an, dass der Druckvorgang nur auf einer Seite des Mediums erfolgt.

</dd> <dt>

**Formular Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Punkte pro Zoll)
</dt> </dl>

Druckauflösung in dpi (Punkte pro Zoll) entlang der x-Achse (Breite) des Druckauftrags (ähnlich der veralteten **XResolution** -Eigenschaft). Dieser Wert wird nur festgelegt, wenn die **PrintQuality** -Eigenschaft dieser Klasse positiv ist.

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Spezifischer Wert einer der drei möglichen Farb Vergleichsmethoden (als Intents bezeichnet), die standardmäßig verwendet werden sollen. ICM-Anwendungen stellen Intents mithilfe der ICM-Funktionen her. Für diese Eigenschaft können vordefinierte Werte von 1 bis 3 oder Treiber definierte Werte von 4 bis 256 angenommen werden. Nicht-ICM-Anwendungen können diesen Wert verwenden, um zu bestimmen, wie der Drucker Farbdruckaufträge verarbeitet.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Sättigung

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Vergleichen Sie

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Exakte Farbe

</dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wie ICM verarbeitet wird. Für eine nicht-ICM-Anwendung bestimmt diese Eigenschaft, ob ICM aktiviert oder deaktiviert ist. Bei ICM-Anwendungen prüft das System diese Eigenschaft, um zu bestimmen, welcher Teil des Computer Systems die ICM-Unterstützung verarbeitet.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Disabled

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Gerätetreiber

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Sicherungsmedium

</dd> </dl>

</dd> <dt>

**Logpixels**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Anzahl der Pixel pro logischem Zoll. Diese veraltete Eigenschaft ist nur für Geräte gültig, die mit Pixeln arbeiten und Geräte wie Drucker ausschließen. Es gibt keinen Ersatzwert, der für Drucker gilt.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Medientyp, auf dem der Drucker druckt. Die-Eigenschaft kann auf einen vordefinierten Wert oder einen Treiber definierten Wert größer oder gleich 256 festgelegt werden.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Standard

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Transparenz

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Glanz

</dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name des Druckers, mit dem diese Konfiguration verknüpft ist. Dieser Wert entspricht der **Name** -Eigenschaft der zugeordneten [**Win32- \_ Drucker**](win32-printer.md) Instanz.

</dd> <dt>

**Ausrichtung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Druck Ausrichtung des Papiers.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Hochformat

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Querformat

</dd> </dl>

</dd> <dt>

**Papier Länge**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Zehntel Millimeter)
</dt> </dl>

Die Länge des Papiers. Um die Größe des Papiers in Zoll zu ermitteln, teilen Sie diesen Wert durch 254.

Beispiel: 2794

</dd> <dt>

**Taschenbuchgröße**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des Papiers. Die möglichen Größen finden Sie in der **Eigenschaft "** Eigenschaft (Eigenschaft)" der zugeordneten [**Win32- \_ Drucker**](win32-printer.md) Klasse.

Beispiel: "A4 oder Buchstabe".

</dd> <dt>

**Taschen Breite**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Zehntel Millimeter)
</dt> </dl>

Breite des Papiers. Um die Größe des Papiers in Zoll zu ermitteln, teilen Sie diesen Wert durch 254.

Beispiel: 2159

</dd> <dt>

**PelsHeight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**PelsWidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine von vier Qualitätsstufen des Druckauftrags. Wenn ein positiver Wert angegeben wird, wird die Qualität in dpi (Punkte pro Zoll) gemessen.

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

Entwurf

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**-2**


</dt> <dd>

Niedrig

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**1-3**


</dt> <dd>

Medium

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**-4**


</dt> <dd>

High

</dd> </dl>

</dd> <dt>

**Skalieren**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Prozent)
</dt> </dl>

Der Faktor, um den die gedruckte Ausgabe skaliert werden soll. Beispielsweise reduziert eine Skala von 75 die Druckausgabe auf 3/4 die ursprüngliche Höhe und Breite.

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

**SpecificationVersion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Versionsnummer der Initialisierungs Daten für das Gerät, das mit dem Windows-basierten Drucker verknüpft ist.

</dd> <dt>

**TTOption**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie TrueType-Schriftarten gedruckt werden sollen.

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)


</dt> <dd>

Druckt TrueType-Schriftarten als Grafiken. Dies ist die Standardaktion für Punkt-Matrix-Drucker.

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)


</dt> <dd>

Lädt TrueType-Schriftarten als weiche Schriftarten herunter. Dies ist die Standardaktion für Drucker, die die druckersteuerungsprache (-PCL) verwenden.

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Ersatz** (3)


</dt> <dd>

Ersetzt Geräte Schriftarten für TrueType-Schriftarten. Dies ist die Standardaktion für PostScript-Drucker.

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Punkte pro Zoll)
</dt> </dl>

Druckauflösung entlang der y-Achse (Höhe) des Druckauftrags (ähnlich der veralteten **YResolution** -Eigenschaft). Dieser Wert wird nur festgelegt, wenn die **PrintQuality** -Eigenschaft dieser Klasse positiv ist.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **HorizontalResolution** -Eigenschaft.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **VerticalResolution** -Eigenschaft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ printerconfiguration** wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

**Übersicht**

Bevor Sie bestimmen können, wie Sie Ihre Druck Ressourcen optimal verteilen und verwenden können, benötigen Sie ausführliche Informationen zu diesen Ressourcen. Beispielsweise kann Abteilung a im Vergleich zu fünf Druckern in Abteilung B nur drei Drucker enthalten. Wenn die Drucker in Abteilung a 20 Seiten pro Minute drucken können und die Drucker in Abteilung B nur 5 Seiten pro Minute drucken können, verfügen Benutzer in Abteilung a tatsächlich über mehr Druckkapazität. Wenn Sie sich nicht mit den detaillierten Funktionen dieser Drucker auskennen, können Sie fälschlicherweise feststellen, dass Abteilung A eine kurze Druckkapazität hat und somit zusätzliche Drucker kaufen, die letztendlich nicht verwendet werden.

WMI umfasst zwei Klassen: [**Win32- \_ Drucker**](win32-printer.md) und **Win32- \_ printerconfiguration**, die verwendet werden können, um detaillierte Informationen zu allen Druckern zurückzugeben, die auf einem Computer installiert sind.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel werden Drucker Informationen abgerufen.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](./cim-setting.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
