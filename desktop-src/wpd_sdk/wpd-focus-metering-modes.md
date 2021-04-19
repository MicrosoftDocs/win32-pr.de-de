---
description: Der \_ Enumerationstyp "WPD-Fokus \_ Messungs \_ Modi" beschreibt, wie ein Gerät entscheiden soll, welcher Teil eines Frames zum Festlegen des Fokus verwendet werden soll.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: WPD_FOCUS_METERING_MODES-Enumeration (portabledevice. h)
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
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355918"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>WPD- \_ Fokus \_ Messungs Modi- \_ Enumeration

Der Enumerationstyp " **WPD- \_ Fokus \_ Messungs \_ Modi** " beschreibt, wie ein Gerät entscheiden soll, welcher Teil eines Frames zum Festlegen des Fokus verwendet werden soll.

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

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD- \_ Fokus \_ Messungs Modus nicht \_ \_ definiert**
</dt> <dd>

Gibt an, dass kein Fokus Modus angegeben wurde.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**Mittelpunkt des WPD- \_ Fokus \_ Messungs \_ Modus \_ \_**
</dt> <dd>

Konzentriert sich auf den Mittelpunkt des eingerahmten Bereichs.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**multiSpot des WPD- \_ Fokus \_ Messungs \_ Modus \_ \_**
</dt> <dd>

Bestimmen Sie den Fokus, indem Sie mehrere Teile des eingerahmten Bereichs analysieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der Eigenschaft für den [ \_ \_ \_ Fokus \_ Messungs \_ Modus der WPD-Bild Größe](still-image-properties.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




