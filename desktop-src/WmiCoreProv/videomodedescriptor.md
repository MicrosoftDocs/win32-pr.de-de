---
description: Enthält Modedeskriptorelemente für das MonitorSourceModes-Array in der WmiMonitorListedSupportedSourceModes-Klasse.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: VideoModeDescriptor-Klasse
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
ms.openlocfilehash: a8f103bf5a23f6e157fc9ecca697c0d1ce7c47bd71be20458d816ca74819dc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558405"
---
# <a name="videomodedescriptor-class"></a>VideoModeDescriptor-Klasse

Die WMI-Klasse **VideoModeDescriptorVideo** enthält Modedeskriptorelemente für das **MonitorSourceModes-Array** in der [**WmiMonitorListedSupportedSourceModes-Klasse.**](wmimonitorlistedsupportedsourcemodes.md) Zu diesen Elementen gehören Überwachungsfunktionen wie Aktualisierungsrate, Pixelmerkmale oder Bildgröße. Die **VideoModeDescriptorVideo-Klasse** enthält Informationen, die eine Obermenge der Daten sind, die von festgelegten, Standard- und detaillierten Zeitsteuerungsblöcken verfügbar sind.

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

Die **VideoModeDescriptor-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **VideoModeDescriptor-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CompositePolarityType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusammengesetzter Polaritätstyp. Dies ist die Polarität horizontaler Synchronisierungsim pulses außerhalb der vertikalen Synchronisierung.



| Wert                                                                              | Bedeutung                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Zusammengesetzte Polarität ist positiv.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Zusammengesetzte Polarität ist negativ.<br/>                                 |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signalsynchronisierungstyp muss digital zusammengesetzt sein.<br/> |



 

</dd> <dt>

**HorizontalActivePixels**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der horizontal aktiven Pixel.

</dd> <dt>

**HorizontalBlankingPixels**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl horizontal leerender Pixel

</dd> <dt>

**HorizontalBorder**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler Rahmen.

</dd> <dt>

**HorizontalImageSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontale Bildgröße in Millimeter (mm).

</dd> <dt>

**HorizontalPolarityType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler Polaritätstyp.



| Wert                                                                              | Bedeutung                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Die horizontale Polarität ist positiv.<br/>                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Die horizontale Polarität ist negativ.<br/>                               |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signalsynchronisierungstyp muss digital getrennt sein.<br/> |



 

</dd> <dt>

**HorizontalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nenner der horizontalen Aktualisierungsrate.

</dd> <dt>

**HorizontalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zähler für horizontale Aktualisierungsrate in Hertz (Hz).

</dd> <dt>

**HorizontalSyncOffset**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Horizontaler Synchronisierungsoffset.

</dd> <dt>

**HorizontalSyncSynchronisierungWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite des horizontalen Synchronisierungsimimens.

</dd> <dt>

**IsInterlaced**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Anzeigemodus übersprungen wird.

</dd> <dt>

**IsSerrationRequired**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt ggf. an, welcher Typ von Serration erforderlich ist.



| Wert                                                                              | Bedeutung                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Der Controller muss während der vertikalen Synchronisierung eine horizontale Synchronisierung bereitstellen.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Der Controller darf während der vertikalen Synchronisierung keine horizontale Synchronisierung bereitstellen.<br/>                             |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signalsynchronisierungstyp muss "1", "Analog Composite" oder "Digital Composite" sein.<br/> |



 

</dd> <dt>

**IsSyncOnRGB**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt ggf. an, welche Videosignallinien synchronisiert werden sollen.



| Wert                                                                              | Bedeutung                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Der Synchronisierungsim pulse sollte auf allen drei Videosignallinien angezeigt werden.<br/>                  |
| <dl> <dt>1 (0x1)</dt> </dl> | Der Synchronisierungsim pulse sollte nur auf der grünen Videosignallinie angezeigt werden.<br/>          |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signalsynchronisierungstyp muss analog zusammengesetzt sein.<br/> |



 

</dd> <dt>

**PixelClockRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pixeltaktfrequenz in Hertz (Hz).

</dd> <dt>

**StereoModeType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stereomodustyp. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                              | Bedeutung                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Keine Stereo-<br/>                                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Sequenzielles Stereofeld mit rechtem Bild bei Stereosynchronisierung.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Sequenzielles Stereofeld mit linker Abbildung bei Stereosynchronisierung.<br/>  |
| <dl> <dt>3 (0x3)</dt> </dl> | 2-Wege-Überlappung von Stereo mit rechtem Bild auf geraden Linien.<br/> |
| <dl> <dt>4 (0x4)</dt> </dl> | 2-Wege-Überlappung von Stereo mit linker Abbildung bei gleichmäßigen Linien.<br/>  |
| <dl> <dt>5 (0x5)</dt> </dl> | 4-Wege-Interleaved Stereo.<br/>                                |
| <dl> <dt>6 (0x6)</dt> </dl> | Side-by-Side Interleaved Stereo.)<br/>                         |



 

</dd> <dt>

**SyncSignalType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Signalsynchronisierungstyp. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                              | Bedeutung                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analog Composite<br/>         |
| <dl> <dt>1 (0x1)</dt> </dl> | Bipolar Analog Composite<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Digital Composite<br/>        |
| <dl> <dt>3 (0x3)</dt> </dl> | Digital Separate<br/>         |



 

</dd> <dt>

**VerticalActivePixels**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl vertikal aktiver Pixel.

</dd> <dt>

**VerticalBlankingPixels**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl vertikal leerer Pixel.

</dd> <dt>

**VerticalBorder**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Rahmen.

</dd> <dt>

**VerticalImageSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikale Bildgröße in Millimeter (mm).

</dd> <dt>

**VerticalPolarityType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Polaritätstyp.



| Wert                                                                              | Bedeutung                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Die vertikale Polarität ist positiv.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Vertikale Polarität ist negativ<br/>                                  |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht zutreffend Der Signalsynchronisierungstyp muss digital getrennt sein.<br/> |



 

</dd> <dt>

**VerticalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nenner der vertikalen Aktualisierungsrate.

</dd> <dt>

**VerticalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zähler für vertikale Aktualisierungsrate in Hertz (Hz).

</dd> <dt>

**VerticalSyncOffset**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikaler Synchronisierungsoffset.

</dd> <dt>

**VerticalSyncSyncSynceWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vertikale Synchronisierungs-Pulsbreite.

</dd> <dt>

VideoStandardType
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Videostandardtyp.



| Wert                                                                                | Bedeutung                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Andere<br/>                                                                                               |
| <dl> <dt>1 (0x1)</dt> </dl>   | VESA DMT. Aus der Spezifikation der Video Electronics Standard Association (VESA) Display Monitor Timings.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>   | VESA GTF. Aus VESA Generalized Timing Formula Standard.<br/>                                            |
| <dl> <dt>3 (0x3)</dt> </dl>   | VESA CVT/Von VESA Coordinated Video Timings Standard.<br/>                                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5)</dt> </dl>   | Apple<br/>                                                                                               |
| <dl> <dt>6 (0x6)</dt> </dl>   | NTSC M<br/>                                                                                              |
| <dl> <dt>7 (0x7)</dt> </dl>   | NTSC J<br/>                                                                                              |
| <dl> <dt>8 (0x8)</dt> </dl>   | NTSC 433<br/>                                                                                            |
| <dl> <dt>9 (0x9)</dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xA)</dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB)</dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xC)</dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD)</dt> </dl>  | PAL I<br/>                                                                                               |
| <dl> <dt>14 (0xE)</dt> </dl>  | PAL D<br/>                                                                                               |
| <dl> <dt>15 (0xF)</dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10)</dt> </dl> | PAL NC<br/>                                                                                              |
| <dl> <dt>17 (0x11)</dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12)</dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13)</dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14)</dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15)</dt> </dl> | SECAM K<br/>                                                                                             |
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
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




