---
title: LB_SETITEMHEIGHT Meldung (Winuser. h)
description: Legt die Höhe von Elementen in einem Listenfeld in Pixel fest. Wenn das Listenfeld den lbs-Besitzer für das- \_ Objekt aufweist, legt diese Meldung die Höhe des durch den wParam-Parameter angegebenen Elements fest. Andernfalls legt diese Meldung die Höhe aller Elemente im Listenfeld fest.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Windows-Steuerelemente für LB_SETITEMHEIGHT Meldung
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
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478540"
---
# <a name="lb_setitemheight-message"></a>LB- \_ Nachricht

Legt die Höhe von Elementen in einem Listenfeld in Pixel fest. Wenn das Listenfeld den [**lbs- \_**](list-box-styles.md) Besitzer für das-Objekt aufweist, legt diese Meldung die Höhe des durch den *wParam* -Parameter angegebenen Elements fest. Andernfalls legt diese Meldung die Höhe aller Elemente im Listenfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index des Elements im Listenfeld an. Verwenden Sie diesen Parameter nur, wenn das Listenfeld [**den \_ lbs**](list-box-styles.md) -Besitzer des "lbs"-Stils aufweist. andernfalls legen Sie es auf NULL fest.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Höhe des Elements in Pixel an. Die maximale Höhe beträgt 255 Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Index oder die Höhe ungültig ist, ist der Rückgabewert lb \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ GetItemHeight**](lb-getitemheight.md)
</dt> </dl>

 

 





