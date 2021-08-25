---
title: LB_SETCURSEL Meldung (Winuser.h)
description: Wählt eine Zeichenfolge aus und scrollt sie bei Bedarf in die Ansicht. Wenn die neue Zeichenfolge ausgewählt ist, entfernt das Listenfeld die Hervorhebung aus der zuvor ausgewählten Zeichenfolge.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33964d98717ab84a325b5070eec6c4e1cacf334ba2272d4691d340a15af78a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085340"
---
# <a name="lb_setcursel-message"></a>LB \_ SETCURSEL-Nachricht

Wählt eine Zeichenfolge aus und scrollt sie bei Bedarf in die Ansicht. Wenn die neue Zeichenfolge ausgewählt ist, entfernt das Listenfeld die Hervorhebung aus der zuvor ausgewählten Zeichenfolge.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den nullbasierten Index der ausgewählten Zeichenfolge an. Wenn dieser Parameter -1 ist, ist das Listenfeld auf keine Auswahl festgelegt.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Das bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Byte nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, lautet der Rückgabewert LB \_ ERR. Wenn der *wParam-Parameter* -1 ist, lautet der Rückgabewert LB \_ ERR, obwohl kein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung nur mit Listenfeldern mit nur einer Auswahl. Sie können sie nicht verwenden, um eine Auswahl in einem Mehrfachauswahllistenfeld festzulegen oder zu entfernen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB \_ GETCURSEL**](lb-getcursel.md)
</dt> </dl>

 

 





