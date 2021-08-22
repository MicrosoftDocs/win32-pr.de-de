---
title: LB_SETITEMHEIGHT (Winuser.h)
description: Legt die Höhe von Elementen in einem Listenfeld in Pixel fest. Wenn das Listenfeld über den LBS OWNERDRAWVARIABLE-Stil verfügt, legt diese Meldung die Höhe des Elements fest, das durch den \_ wParam-Parameter angegeben wird. Andernfalls legt diese Meldung die Höhe aller Elemente im Listenfeld fest.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd661c9fb32d2cbe0763f8c138d133f8a32b46d17201b33033b832aeb8cb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433870"
---
# <a name="lb_setitemheight-message"></a>LB \_ SETITEMHEIGHT-Nachricht

Legt die Höhe von Elementen in einem Listenfeld in Pixel fest. Wenn das Listenfeld über den [**LBS \_ OWNERDRAWVARIABLE-Stil**](list-box-styles.md) verfügt, legt diese Meldung die Höhe des Elements fest, das durch den *wParam-Parameter angegeben* wird. Andernfalls legt diese Meldung die Höhe aller Elemente im Listenfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den nullbasierten Index des Elements im Listenfeld an. Verwenden Sie diesen Parameter nur, wenn das Listenfeld über den [**LBS \_ OWNERDRAWVARIABLE-Stil**](list-box-styles.md) verfügt, andernfalls legen Sie ihn auf 0 (null) fest.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Höhe des Elements in Pixel an. Die maximale Höhe beträgt 255 Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Index oder die Höhe ungültig ist, ist der Rückgabewert LB \_ ERR.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)
</dt> </dl>

 

 





