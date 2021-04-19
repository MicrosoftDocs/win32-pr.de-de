---
description: Der \_ Enumerationstyp der WPD-Effekt \_ Modi beschreibt verschiedene visuelle Effekte, die auf ein Bild angewendet werden können.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: WPD_EFFECT_MODES-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360259"
---
# <a name="wpd_effect_modes-enumeration"></a>WPD- \_ Effekt \_ Modi-Enumeration

Der Enumerationstyp der **WPD- \_ Effekt \_ Modi** beschreibt verschiedene visuelle Effekte, die auf ein Bild angewendet werden können.

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

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD- \_ Effekt \_ Modus nicht \_ definiert**
</dt> <dd>

Es wurde keine Auswirkung angegeben.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**Farbe für WPD- \_ Effekt \_ Modus \_**
</dt> <dd>

Das Bild sollte "Color" lauten.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD \_ \_ -Effekt Modus \_ schwarz \_ und \_ weiß**
</dt> <dd>

Das Bild sollte Schwarz und weiß sein.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD- \_ Effekt Modus (* \_ \_ Pia)**
</dt> <dd>

Das Bild sollte "* Pia" lauten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der Eigenschaft " [ \_ immer noch \_ Bild \_ Effekt \_ Modus](still-image-properties.md) " verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




