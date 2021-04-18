---
description: Der \_ Enumerationstyp für WPD-White \_ Balance- \_ Einstellungen beschreibt, wie ein Video-oder Bild-Gerät Farbkanäle gewichtet, um einen geeigneten weißen Saldo zu erzielen
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: WPD_WHITE_BALANCE_SETTINGS-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372344"
---
# <a name="wpd_white_balance_settings-enumeration"></a>WPD \_ - \_ Enumeration für weiß Balance- \_ Einstellungen

Der Enumerationstyp für **WPD- \_ White \_ Balance- \_ Einstellungen** beschreibt, wie ein Video-oder Bild-Gerät Farbkanäle gewichtet, um einen geeigneten weißen Saldo zu erzielen

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

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD- \_ weißen \_ Saldo nicht \_ definiert**
</dt> <dd>

Dieser Wert wurde nicht definiert.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD \_ - \_ WhiteBalance \_ manuell**
</dt> <dd>

Der weiße Saldo wird explizit mit der-Eigenschaft für den Bild-und Bild-Wert von WPD festgelegt und wird nicht selbst geändert. [ \_ \_ \_ \_ ](still-image-properties.md)

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD- \_ weiß- \_ Ausgleich \_ automatisch**
</dt> <dd>

Das Gerät legt den weißen Saldo fest.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD- \_ weiß- \_ Ausgleich \_ 1 \_ Push \_ automatisch**
</dt> <dd>

Das Gerät legt den weißen Saldo fest, aber nur, wenn der Benutzer die Erfassungs Schaltfläche des Geräts drückt, während er das Gerät in einem weißen Feld anzielt.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ weiß \_ Balance- \_ Sommerzeit**
</dt> <dd>

Auf dem Gerät werden die in den meisten Sommerzeit Einstellungen geeigneten weißen Ausgleichs Nummern verwendet.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD- \_ weiß \_ Balance- \_ Wolfram**
</dt> <dd>

Auf dem Gerät werden die in den meisten Umgebungen für das Incandescent-Beleuchtungs Verfahren verwendeten weißen Ausgleichs Nummern verwendet.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD- \_ weiß \_ Balance \_ Flash**
</dt> <dd>

Auf dem Gerät werden die für die Verwendung mit einem Flash geeigneten weißen Ausgleichs Nummern verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der WPD-Eigenschaft für den [ \_ \_ \_ weißen \_ Saldo weiterhin](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




