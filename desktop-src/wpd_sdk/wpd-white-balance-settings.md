---
description: Der WPD WHITE BALANCE SETTINGS-Enumerationstyp beschreibt, wie ein Video- oder Bildgerät Farbkanäle \_ \_ gewichtet, um einen \_ ordnungsgemäßen Weißabgleich zu erzielen.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: WPD_WHITE_BALANCE_SETTINGS -Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842047"
---
# <a name="wpd_white_balance_settings-enumeration"></a>WPD \_ WHITE \_ BALANCE \_ SETTINGS-Enumeration

Der **WPD \_ WHITE BALANCE \_ SETTINGS-Enumerationstyp \_** beschreibt, wie ein Video- oder Bildgerät Farbkanäle gewichtet, um einen ordnungsgemäßen Weißabgleich zu erzielen.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD \_ WHITE \_ BALANCE \_ UNDEFINED**
</dt> <dd>

Dieser Wert wurde nicht definiert.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD \_ WHITE \_ BALANCE \_ MANUAL**
</dt> <dd>

Der Weißabgleich wird explizit mithilfe der [WPD \_ STILL IMAGE \_ RGB \_ \_ GAIN-Eigenschaft](still-image-properties.md) festgelegt und ändert sich nicht allein.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ AUTOMATIC**
</dt> <dd>

Das Gerät wird den Weißabgleich festlegen.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ ONE \_ PUSH \_ AUTOMATIC**
</dt> <dd>

Das Gerät wird den Weißabgleich festlegen, aber nur, wenn der Benutzer die Erfassungsschaltfläche des Geräts drückt, während das Gerät auf ein weißes Feld zielt.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ WHITE \_ BALANCE \_ DAYLIGHT**
</dt> <dd>

Das Gerät verwendet Für die meisten Sommerzeiteinstellungen geeignete White balance-Nummern.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_WPD-WHITE \_ \_ BALANCE- VERALTEN**
</dt> <dd>

Das Gerät verwendet Weißabgleichnummern, die für die verwendung in den meisten Beleuchtungseinstellungen für Glühbirnen geeignet sind.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD \_ WHITE \_ BALANCE \_ FLASH**
</dt> <dd>

Das Gerät verwendet für die Verwendung mit einem Flash geeignete White balance-Nummern.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ STILL IMAGE \_ WHITE \_ \_ BALANCE-Eigenschaft](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




