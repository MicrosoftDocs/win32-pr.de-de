---
description: Der \_ Enumerationstyp der WPD-Flash \_ Modi beschreibt einen Flash Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden soll.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: WPD_FLASH_MODES-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372100"
---
# <a name="wpd_flash_modes-enumeration"></a>WPD- \_ Flash \_ Modi-Enumeration

Der Enumerationstyp der **WPD- \_ Flash \_ Modi** beschreibt einen Flash Modus, der beim Erfassen von Bildern mit einem Gerät verwendet werden soll.

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

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD- \_ Flash \_ Modus nicht \_ definiert**
</dt> <dd>

Es wurde kein Flash-Modus angegeben.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD- \_ Flash \_ Modus \_ automatisch**
</dt> <dd>

Gibt an, dass der Flash im automatischen Modus verwendet werden soll, wie vom Gerät angegeben.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD- \_ Flash \_ Modus \_ Off**
</dt> <dd>

Gibt an, dass kein Flash verwendet werden soll.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**Füllung des WPD- \_ Flash \_ Modus \_**
</dt> <dd>

Gibt einen Flash Füll Typ an.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD- \_ Flash \_ Modus " \_ Red \_ Eye \_ Auto"**
</dt> <dd>

Gibt an, dass die rote Augen Reduzierungs-Flash verwendet werden soll.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_ \_ \_ Red \_ Eye \_ Fill im WPD-Flash Modus**
</dt> <dd>

Gibt an, dass der Rote Augen Füll Blitz verwendet werden soll.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ \_ externe \_ Synchronisierung im WPD-Flash Modus**
</dt> <dd>

Gibt an, dass der Flash mit anderen externen Flash Geräten synchronisiert werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der [WPD- \_ \_ Image- \_ Flash \_ Mode](still-image-properties.md) -Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




