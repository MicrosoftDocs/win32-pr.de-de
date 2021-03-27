---
description: Diese Klasse ist die Ereignistyp Klasse für Video Konfigurations Ereignisse.
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 370c67501b75f0fd4ac88488744280f1e0065bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980944"
---
# <a name="systemconfig_video-class"></a>SystemConfig- \_ Video Klasse

Diese Klasse ist die Ereignistyp Klasse für Video Konfigurations Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
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

Die **SystemConfig- \_ Video** Klasse enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig- \_ Video** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Adapterstring**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (8), **Max** (256), **Format ("s")**
</dt> </dl>

Der Name oder die Beschreibung des Adapters.

</dd> <dt>

**Biosstring**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (9), **Max** (256), **Format ("s")**
</dt> </dl>

BIOS-Name des Adapters.

</dd> <dt>

**Bitsper Pixel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4)
</dt> </dl>

Anzahl von Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.

</dd> <dt>

**Chiptyp**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6), **Max** (256), **Format ("s")**
</dt> </dl>

Der Chip Name des Adapters.

</dd> <dt>

**' Dactype '**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (7), **Max** (256), **Format ("s")**
</dt> </dl>

Der DAC-Chip Name (Digital-to-Analog Converter) des Adapters.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (10), **Max** (256), **Format ("s")**
</dt> </dl>

Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1)
</dt> </dl>

Maximal unterstützte Arbeitsspeicher Größe in Bytes.

</dd> <dt>

**Stateflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (11), **Format ("x")**
</dt> </dl>

Gerätestatusflags. Dabei kann es sich um eine beliebige Kombination der folgenden handelt.



| Wert                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**Anzeigen \_ \_ \_ An \_ Desktop angefügtes Gerät**</dt> <dt>1 (0x1)</dt> </dl> | Das Gerät ist Teil des Desktops.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**Anzeigen \_ Geräte \_ Spiegelungs \_ Treiber**</dt> <dt>8 (0x8)</dt> </dl>           | Stellt ein Pseudo Gerät dar, das verwendet wird, um die Anwendungs Zeichnung für die Verbindung mit einem Remote Computer oder anderen Zwecken zu spiegeln. Diesem Gerät ist ein unsichtbarer Pseudo Monitor zugeordnet. Beispielsweise verwendet NetMeeting Sie.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**Anzeigen \_ Gerät \_ modespruned**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | Das Gerät verfügt über mehr Anzeigemodi als von seinen Ausgabegeräten unterstützt wird.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**Anzeigen \_ \_Primäres \_**</dt> Gerät <dt>4 (0x4)</dt> </dl>                 | Der primäre Desktop befindet sich auf dem Gerät. Bei einem System mit einer einzelnen Anzeigekarte wird dies immer festgelegt. Bei einem System mit mehreren Anzeige Karten kann dieser Satz nur von einem Gerät festgelegt werden.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**Anzeigen \_ Gerät \_**</dt> Wechsel <dt>32 (0x20)</dt> </dl>                               | Das Gerät ist austauschbar. Dies kann nicht die primäre Anzeige sein.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**Anzeigen \_ Gerät \_ VGA- \_ kompatibel**</dt> <dt>16 (0x10)</dt> </dl>               | Das Gerät ist VGA-kompatibel.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5)
</dt> </dl>

Aktuelle Aktualisierungsrate in Hertz.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2)
</dt> </dl>

Aktuelle Anzahl von horizontalen Pixeln.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3)
</dt> </dl>

Aktuelle Anzahl vertikaler Pixel.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




