---
description: Der \_ WPD FOCUS \_ METERING \_ MODES-Enumerationstyp beschreibt, wie ein Gerät entscheiden soll, welcher Teil eines Frames verwendet werden soll, um den Fokus festzulegen.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: WPD_FOCUS_METERING_MODES-Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: eb37cdd32673c385617d9c0c0ae8616c8dae0ab711d1253391ae2c1e6b2f8789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703770"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>WPD \_ FOCUS \_ METERING \_ MODES-Enumeration

Der **WPD \_ FOCUS \_ METERING \_ MODES-Enumerationstyp** beschreibt, wie ein Gerät entscheiden soll, welcher Teil eines Frames verwendet werden soll, um den Fokus festzulegen.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD \_ FOCUS \_ METERING \_ MODE \_ UNDEFINED**
</dt> <dd>

Gibt an, dass kein Fokussiermodus angegeben wurde.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD \_ FOCUS \_ METERING \_ MODE \_ CENTER \_ SPOT**
</dt> <dd>

Konzentriert sich auf die Mitte des Umrandungsbereichs.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD \_ FOCUS \_ METERING \_ MODE \_ MULTI \_ SPOT**
</dt> <dd>

Bestimmen Sie den Fokus, indem Sie mehrere Teile des Umrandungsbereichs analysieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ STILL IMAGE \_ FOCUS \_ \_ METERING \_ MODE-Eigenschaft](still-image-properties.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




