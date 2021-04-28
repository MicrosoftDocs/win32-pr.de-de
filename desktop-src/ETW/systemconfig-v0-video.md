---
description: 'SystemConfig_V0_Video-Klasse: Diese Klasse ist die Ereignistypklasse für Videokonfigurationsereignisse.'
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94fb9e50344cfbdde4be67815b80e4074ab1a878
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105918"
---
# <a name="systemconfig_v0_video-class"></a>SystemConfig \_ V0 \_ Video-Klasse

Diese Klasse ist die Ereignistypklasse für Videokonfigurationsereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ V0 \_ Video-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ V0 \_ Video-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (8), **Max** (256)
</dt> </dl>

Name oder Beschreibung des Adapters.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (9), **Max** (256)
</dt> </dl>

BIOS-Name des Adapters.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Anzahl der Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Chipname des Adapters.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7), **Max** (256)
</dt> </dl>

Der Name des DAC-Chips (Digital-to-Analog Converter) des Adapters.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Adresse oder andere identifizierende Informationen zum eindeutigen Benennen des logischen Geräts.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1)
</dt> </dl>

Maximal unterstützter Arbeitsspeicher in Bytes.

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

Gerätestatusflags. Dies kann eine beliebige kombination der folgenden Punkte sein.



| Wert                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**DISPLAY \_ AN DESKTOP 1 \_ \_ \_ ANGESCHLOSSENES GERÄT**</dt> <dt>(0X1)</dt> </dl> | Das Gerät ist Teil des Desktops.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**DISPLAY \_ \_GERÄTESPIEGELUNGSTREIBER \_**</dt> <dt>8 (0x8)</dt> </dl>           | Stellt ein Pseudogerät dar, das zum Spiegeln von Anwendungszeichnungen zum Herstellen einer Verbindung mit einem Remotecomputer oder anderen Zwecken verwendet wird. Diesem Gerät ist ein unsichtbarer Pseudomonitor zugeordnet. NetMeeting verwendet sie beispielsweise.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**DISPLAY \_ \_GERÄTEMODUSSPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | Das Gerät verfügt über mehr Anzeigemodi als die Ausgabegeräte unterstützen.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**DISPLAY \_ \_PRIMÄRES \_ GERÄT**</dt> <dt>4 (0x4)</dt> </dl>                 | Der primäre Desktop befindet sich auf dem Gerät. Für ein System mit einer einzelnen Anzeigekarte ist dies immer festgelegt. Für ein System mit mehreren Grafikkarten kann diese Einstellung nur auf einem Gerät festgelegt werden.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**DISPLAY \_ DEVICE \_ REMOVABLE**</dt> <dt>32 (0x20)</dt> </dl>                               | Das Gerät ist wechselbar. es kann nicht die primäre Anzeige sein.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**DISPLAY \_ \_ \_ GERÄTE-VGA-KOMPATIBEL**</dt> <dt>16 (0x10)</dt> </dl>               | Das Gerät ist VGA-kompatibel.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Aktuelle Aktualisierungsrate in Hertz.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Aktuelle Anzahl horizontaler Pixel.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Aktuelle Anzahl vertikaler Pixel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




