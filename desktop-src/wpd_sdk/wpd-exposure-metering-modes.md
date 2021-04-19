---
description: Der \_ \_ Enumerationstyp der WPD-aufgabenmessungs- \_ Modi beschreibt den Messungs Modus, der verwendet werden soll, wenn die Verfügbarkeit der Bild Erfassung durch ein Gerät
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: WPD_EXPOSURE_METERING_MODES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370132"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>Enumeration der WPD- \_ Expositions \_ Messungs \_ Modi

Der Enumerationstyp der **WPD-aufgabenmessungs- \_ \_ \_ Modi** beschreibt den Messungs Modus, der verwendet werden soll, wenn die Verfügbarkeit der Bild Erfassung durch ein Gerät

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD \_ - \_ \_ aufwirkungs Messungs Modus nicht \_ definiert**
</dt> <dd>

Der Messungs Modus ist nicht definiert.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**Durchschnitt des WPD- \_ Expositions \_ Messungs \_ Modus \_**
</dt> <dd>

Verwenden Sie die durchschnittliche Verfügbarkeit im gesamten Image.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**mittlere Mittelwert des WPD- \_ Expositions \_ Messungs \_ Modus \_ \_ \_**
</dt> <dd>

Verwenden Sie eine durchschnittliche Verfügbarkeit, bei der der Mittelpunkt des Bilds stärker gewichtet wird.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**multiSpot für den WPD- \_ Expositions \_ Messungs \_ Modus \_ \_**
</dt> <dd>

Verwenden Sie eine mehrstufige Mittelpunkt Technik.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**Mittelpunkt des WPD- \_ Expositions \_ Messungs \_ Modus \_ \_**
</dt> <dd>

Verwenden Sie eine Mittelpunkt-Mittelpunkt Technik.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Gibt den Messungs Modus des Geräts an. Diese Enumeration wird von der WPD-Eigenschaft für die Aufzählungs [ \_ \_ \_ \_ \_ Messung des Bilds](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




