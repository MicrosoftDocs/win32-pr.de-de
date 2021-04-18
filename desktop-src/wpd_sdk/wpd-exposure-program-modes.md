---
description: Der \_ \_ \_ Enumerationstyp der WPD-aufgabenprogrammebeschreibt einen Bereitstellungs Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: WPD_EXPOSURE_PROGRAM_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372101"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>WPD \_ - \_ \_ Aufzählungs Programmmodi-Enumeration

Der Enumerationstyp der WPD-aufgabenprogrammebeschreibt einen Bereitstellungs Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden **\_ \_ \_**

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD \_ - \_ renderingprogrammmodus nicht \_ \_ definiert**
</dt> <dd>

Der Anzeigemodus wurde nicht angegeben.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD \_ - \_ \_ aufstellungsprogrammmodus \_ manuell**
</dt> <dd>

Die Anwendung sollte alle Einstellungen für das verfügbar machen.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD \_ - \_ \_ aufwirkungs Programmmodus \_ automatisch**
</dt> <dd>

Verwenden Sie einen Geräte definierten automatischen Funktionsmodus.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**Öffnungs Priorität des WPD- \_ \_ renderingprogrammmodus \_ \_ \_**
</dt> <dd>

Ein automatisierter Anzeigemodus, der angibt, dass der Wert für die lichtöffnung festgelegt bleiben soll, aber die Auswertungs Geschwindigkeit vom Gerät bestimmt werden soll.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**Auslöse Priorität für den WPD- \_ \_ auflockprogrammmodus \_ \_ \_**
</dt> <dd>

Ein automatisierter Anzeigemodus, der angibt, dass die Auslösegeschwindigkeit korrigiert bleiben soll, diese aber vom Gerät bestimmt werden soll.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ - \_ renderingprogrammmodus- \_ \_ kreativ**
</dt> <dd>

Ein automatisierter Anzeigemodus, der versucht, die Tiefe des Felds zu maximieren.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**Aktion für den WPD-aufwirkungs \_ \_ Programm \_ Modus \_**
</dt> <dd>

Ein automatisierter Anzeigemodus, der versucht, die Auslösegeschwindigkeit zu maximieren.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**Hochformat des WPD- \_ \_ \_ aufwirkungs Programms \_**
</dt> <dd>

Ein automatisierter Anzeigemodus, der eine relativ flache Tiefe von Feldern angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Gibt den aufgeräteregistrierungs Modus des Geräts an. Diese Enumeration wird von der WPD-Eigenschaft zum [ \_ \_ \_ \_ renderingprogrammmodus \_ weiterhin](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




