---
description: Enthält modusdeskriptorelemente für das monitorsourcemodes-Array in der wmimonitorlistedsupportedsourcemodes-Klasse.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Videomodedescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348428"
---
# <a name="videomodedescriptor-class"></a>Videomodedescriptor-Klasse

Die **videomodedescriptorvideo** -WMI-Klasse enthält modusdeskriptorelemente für das **monitorsourcemodes** -Array in der [**wmimonitorlistedsupportedsourcemodes**](wmimonitorlistedsupportedsourcemodes.md) -Klasse. Zu diesen Elementen gehören Monitor Features wie Aktualisierungsrate, Pixel Merkmale oder die Bildgröße. Die **videomodedescriptorvideo** -Klasse enthält Informationen, die eine übergeordnete Menge der Daten sind, die aus eingerichteten, standardmäßigen und detaillierten Zeit Steuerungs Blöcken verfügbar sind.

## <a name="syntax"></a>Syntax

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a>Member

Die **videomodedescriptor** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **videomodedescriptor** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Compositepolaritytype**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusammengesetzter poltyp. Dies ist eine Polarität von horizontalen Synchronisierungs Impulsen außerhalb der vertikalen Synchronisierung.



| Wert                                                                              | Bedeutung                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Die zusammengesetzte Polarität ist positiv.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Die zusammengesetzte Polarität ist negativ.<br/>                                 |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signal Synchronisierungstyp muss Digital Composite sein.<br/> |



 

</dd> <dt>

**Horizontalactivepixels**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl von horizontal aktiven Pixeln.

</dd> <dt>

**Horizontalblankingpixels**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der horizontal leere Pixel

</dd> <dt>

**Horizontalborder**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler Rahmen.

</dd> <dt>

**Horizontalimagesize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontale Bildgröße in Millimeter (mm).

</dd> <dt>

**Horizontalpolaritytype**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler poltyp.



| Wert                                                                              | Bedeutung                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Die horizontale Polarität ist positiv.<br/>                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Die horizontale Polarität ist negativ.<br/>                               |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signal Synchronisierungstyp muss Digital getrennt sein.<br/> |



 

</dd> <dt>

**Horizontalfreshshratenenner**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Nenner der horizontalen Aktualisierungsrate.

</dd> <dt>

**Horizontalfreshshratenumschlag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler Aktualisierungs Raten Zähler in Hertz (Hz).

</dd> <dt>

**Horizontalsyncoffset**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler Synchronisierungs Offset.

</dd> <dt>

**Horizontalsyncpull Width**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite der horizontalen Synchronisierungs Pulse.

</dd> <dt>

**Isinterschnür**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Anzeigemodus mit Zeilen Sprung verbunden ist.

</dd> <dt>

**Isserrationrequired**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt ggf. an, welche Art von Server erforderlich ist.



| Wert                                                                              | Bedeutung                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Der Controller muss während der vertikalen Synchronisierung eine horizontale Synchronisierung angeben.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Der Controller darf während der vertikalen Synchronisierung keine horizontale Synchronisierung bereitstellen.<br/>                             |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signal Synchronisierungstyp muss ein Bipolar, ein Analog zusammengesetzter oder ein digitaler Verbund sein.<br/> |



 

</dd> <dt>

**Issynconfiguration**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt ggf. an, welche Videosignal Linien synchronisiert werden sollen.



| Wert                                                                              | Bedeutung                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Der Synchronisierungs Impuls sollte in allen drei Videosignal Zeilen angezeigt werden.<br/>                  |
| <dl> <dt>1 (0x1)</dt> </dl> | Der Synchronisierungs Impuls sollte nur in der grünen Videosignal Linie angezeigt werden.<br/>          |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signal Synchronisierungstyp muss eine bipolare, zusammengesetzte Zeichen<br/> |



 

</dd> <dt>

**Pixelclockrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pixel Taktfrequenz in Hertz (Hz).

</dd> <dt>

**Stereomodetype**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ des Stereo-Modus. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                              | Bedeutung                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Keine Stereo-.<br/>                                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Feld sequenzielles Stereo mit dem richtigen Bild bei der Stereo Synchronisierung.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Feld sequenzielles Stereo mit Links Bild bei der Stereo-Synchronisierung.<br/>  |
| <dl> <dt>3 (0x3)</dt> </dl> | bidirektionale verschachtelte Stereo-Stereo-Datei mit dem rechten Bild in geraden Linien.<br/> |
| <dl> <dt>4 (0x4)</dt> </dl> | bidirektionale verschachtelte Stereo-Stereo-Datei mit dem linken Bild in geraden Linien.<br/>  |
| <dl> <dt>5 (0x5)</dt> </dl> | vier Wege verschachtelte Stereo<br/>                                |
| <dl> <dt>6 (0x6)</dt> </dl> | Paralleles Interleaved Stereo.<br/>                         |



 

</dd> <dt>

**Syncsignaltype**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Signal Synchronisierungstyp. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                              | Bedeutung                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analog zusammengesetzter<br/>         |
| <dl> <dt>1 (0x1)</dt> </dl> | Bipolar Analog Composite<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Digitaler Verbund<br/>        |
| <dl> <dt>3 (0x3)</dt> </dl> | Digitaler separater<br/>         |



 

</dd> <dt>

**Verticalactivepixels**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl von vertikal aktiven Pixeln.

</dd> <dt>

**Verticalblankingpixels**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl von vertikal Leerlauf enden Pixeln.

</dd> <dt>

**Verticalborder**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Rahmen.

</dd> <dt>

**Vertikalimagesize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikale Bildgröße in Millimeter (mm).

</dd> <dt>

**Verticalpolaritytype**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler poltyp.



| Wert                                                                              | Bedeutung                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Die vertikale Polarität ist positiv.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Vertikale Polarität ist negativ.<br/>                                  |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signal Synchronisierungstyp muss Digital getrennt sein.<br/> |



 

</dd> <dt>

**Verticalfreshshratenenner**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Aktualisierungs Raten Nenner.

</dd> <dt>

**Verticalcalfreshatenumschlag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Aktualisierungs Raten Zähler in Hertz (Hz).

</dd> <dt>

**Verticalsyncoffset**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Synchronisierungs Offset.

</dd> <dt>

**Verticalsyncpulcalwidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite der vertikalen Synchronisierungs Pulse.

</dd> <dt>

Videostandardtype
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Video-Standardtyp.



| Wert                                                                                | Bedeutung                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Sonstiges<br/>                                                                                               |
| <dl> <dt>1 (0x1)</dt> </dl>   | VESA-DMT. Von der Grafik zur Anzeige des Monitor Zeit Monitors für die Video-Electronics Standard Association (VESA).<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>   | VESA-GTF. Von VESA verallgemeinerter Zeit Formel Standard.<br/>                                            |
| <dl> <dt>3 (0x3)</dt> </dl>   | VESA CVT/von VESA koordinierte Video Zeitstandard.<br/>                                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5)</dt> </dl>   | Apples<br/>                                                                                               |
| <dl> <dt>6 (0x6)</dt> </dl>   | NTSC M<br/>                                                                                              |
| <dl> <dt>7 (0x7)</dt> </dl>   | NTSC J<br/>                                                                                              |
| <dl> <dt>8 (0x8)</dt> </dl>   | NTSC 433<br/>                                                                                            |
| <dl> <dt>9 (0x9)</dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xa)</dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB)</dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xc)</dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD)</dt> </dl>  | PAL I<br/>                                                                                               |
| <dl> <dt>14 (0xe)</dt> </dl>  | PAL-ID<br/>                                                                                               |
| <dl> <dt>15 (0xF)</dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10)</dt> </dl> | PAL-NC<br/>                                                                                              |
| <dl> <dt>17 (0x11)</dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12)</dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13)</dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14)</dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15)</dt> </dl> | SECAM-K<br/>                                                                                             |
| <dl> <dt>22 (0x16)</dt> </dl> | SECAM K1<br/>                                                                                            |
| <dl> <dt>23 (0x17)</dt> </dl> | SECAM L<br/>                                                                                             |
| <dl> <dt>24 (0x18)</dt> </dl> | SECAM L1<br/>                                                                                            |
| <dl> <dt>25 (0x19)</dt> </dl> | EIA861<br/>                                                                                              |
| <dl> <dt>26 (0x1A)</dt> </dl> | EIA861A<br/>                                                                                             |
| <dl> <dt>27 (0x1B)</dt> </dl> | EIA861B<br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




