---
description: Der Enumerationstyp WPD \_ EXPOSURE PROGRAM MODES beschreibt einen Belichtungsmodus, der beim Erfassen von Bildern \_ mit einem Gerät verwendet werden \_ kann.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: WPD_EXPOSURE_PROGRAM_MODES -Enumeration (PortableDevice.h)
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
ms.openlocfilehash: dc64012c4f13f84abef55d2426c856b931eb447e61df4f04c69781c089857930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083274"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>WPD \_ EXPOSURE \_ PROGRAM \_ MODES-Enumeration

Der **Enumerationstyp WPD \_ EXPOSURE PROGRAM \_ \_ MODES** beschreibt einen Belichtungsmodus, der beim Erfassen von Bildern mit einem Gerät verwendet werden kann.

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

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD \_ EXPOSURE PROGRAM MODE \_ \_ \_ UNEFINED**
</dt> <dd>

Der Belichtungsmodus wurde nicht angegeben.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ MANUAL**
</dt> <dd>

Die Anwendung sollte alle Belichtungseinstellungen angeben.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ AUTO**
</dt> <dd>

Verwenden Sie einen gerätedefinierten automatischen Belichtungsmodus.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ APERTURE \_ PRIORITY**
</dt> <dd>

Ein automatisierter Belichtungsmodus, der angibt, dass der Wert der Blende der Brille fest bleiben soll, aber die Geschwindigkeit der Drehung sollte vom Gerät bestimmt werden.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD \_ EXPOSURE PROGRAM MODE PRIORITY \_ (PRIORITÄT DES \_ \_ WPD-BELICHTUNGSPROGRAMMSMODUS) \_**
</dt> <dd>

Ein automatisierter Belichtungsmodus, der angibt, dass die Drehgeschwindigkeit fest bleiben soll, diese Blende jedoch vom Gerät bestimmt werden sollte.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ CREATIVE**
</dt> <dd>

Ein automatisierter Belichtungsmodus, der versucht, die Feldtiefe zu maximieren.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**AKTION "WPD \_ EXPOSURE \_ PROGRAM \_ MODE" (WPD-BELICHTUNGSPROGRAMMMODUS) \_**
</dt> <dd>

Ein automatisierter Belichtungsmodus, der versucht, die Geschwindigkeit der Brille zu maximieren.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD \_ EXPOSURE PROGRAM MODE \_ \_ \_ HOCHFORMAT**
</dt> <dd>

Ein automatisierter Belichtungsmodus, der eine relativ flache Feldtiefe angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Gibt den Belichtungsprogrammmodus des Geräts an. Diese Enumeration wird von der [WPD \_ STILL IMAGE EXPOSURE PROGRAM \_ \_ \_ \_ MODE-Eigenschaft](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




