---
description: Der WPD \_ EFFECT \_ MODES-Enumerationstyp beschreibt verschiedene visuelle Effekte, die auf ein Bild angewendet werden können.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: WPD_EFFECT_MODES -Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8ca712a758d23f70d2a1f8760272b821adeec548a1d719c9564cdc8cf17cdeb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657420"
---
# <a name="wpd_effect_modes-enumeration"></a>WPD \_ EFFECT \_ MODES-Enumeration

Der **WPD \_ EFFECT \_ MODES-Enumerationstyp** beschreibt verschiedene visuelle Effekte, die auf ein Bild angewendet werden können.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_ \_ WPD-EFFEKTMODUS \_ NICHT DEFINIERT**
</dt> <dd>

Es wurde keine Auswirkung angegeben.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD \_ EFFECT \_ MODE \_ COLOR**
</dt> <dd>

Das Bild sollte eine Farbe haben.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_ \_ WPD-EFFEKTMODUS \_ SCHWARZ UND \_ \_ WEIß**
</dt> <dd>

Das Bild sollte schwarz und weiß sein.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD \_ EFFECT \_ MODE \_ SEPIA**
</dt> <dd>

Das Bild sollte sepia sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ STILL IMAGE \_ EFFECT \_ \_ MODE-Eigenschaft](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




