---
description: Der \_ Enumerationstyp des WPD-Fokus \_ Modus beschreibt den Fokus Modus, der von einem Bild Erfassungsgerät verwendet wird.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: WPD_FOCUS_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370155"
---
# <a name="wpd_focus_modes-enumeration"></a>WPD- \_ Fokus \_ Modi-Enumeration

Der Enumerationstyp des **WPD- \_ Fokus \_** Modus beschreibt den Fokus Modus, der von einem Bild Erfassungsgerät verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD- \_ Fokus nicht \_ definiert**
</dt> <dd>

Der Fokus Modus wurde nicht angegeben.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD- \_ Fokus \_ manuell**
</dt> <dd>

Gibt den manuellen Fokus an.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD- \_ Fokus \_ automatisch**
</dt> <dd>

Gibt den automatischen Fokus an, der vom Gerät gesteuert wird.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**Automatisches WPD- \_ Fokus- \_ \_ Makro**
</dt> <dd>

Gibt an, dass das Gerät nach Bedarf automatisch zwischen Makro und normalem Fokus wechseln soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der Eigenschaft für den [ \_ \_ \_ Fokus \_ Modus des WPD-Bilds](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




