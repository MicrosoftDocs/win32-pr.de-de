---
description: Der WPD \_ FLASH \_ MODES-Enumerationstyp beschreibt einen Flashmodus, der beim Erfassen von Bildern mit einem Gerät verwendet werden soll.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: WPD_FLASH_MODES-Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72e9b6cb2b52f1d90c584b6f425711769b25ea0c5d44065b5aa377d2811592e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005920"
---
# <a name="wpd_flash_modes-enumeration"></a>WPD \_ FLASH \_ MODES-Enumeration

Der **WPD \_ FLASH \_ MODES-Enumerationstyp** beschreibt einen Flashmodus, der beim Erfassen von Bildern mit einem Gerät verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD \_ FLASH \_ MODE \_ UNDEFINED**
</dt> <dd>

Es wurde kein Flashmodus angegeben.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD \_ FLASH \_ MODE \_ AUTO**
</dt> <dd>

Gibt an, dass der Flash im automatischen Modus verwendet werden soll, wie vom Gerät angegeben.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD \_ FLASH \_ MODE \_ OFF**
</dt> <dd>

Gibt an, dass kein Flash verwendet werden soll.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD \_ FLASH \_ MODE \_ FILL**
</dt> <dd>

Gibt einen Flash vom Typ "Fill" an.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD \_ FLASH \_ MODE \_ RED \_ EYE \_ AUTO**
</dt> <dd>

Gibt an, dass der Blinken der Roten Augenverringerung verwendet werden soll.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD \_ FLASH \_ MODE \_ RED \_ EYE \_ FILL**
</dt> <dd>

Gibt an, dass der Blitz mit roter Augenfüllung verwendet werden soll.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**EXTERNE \_ \_ \_ \_ SYNCHRONISIERUNG IM WPD-FLASHMODUS**
</dt> <dd>

Gibt an, dass der Flash mit anderen externen Flashgeräten synchronisiert werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ STILL IMAGE \_ FLASH \_ \_ MODE-Eigenschaft](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




