---
title: LB_SELITEMRANGEEX Meldung (Winuser.h)
description: Wählt mindestens ein aufeinander folgendes Element in einem Listenfeld mit mehrfacher Auswahl aus.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e3112e36a7b212c1d0968ca738472000fabbf3d26d4d94e36ea9f21d80fe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799440"
---
# <a name="lb_selitemrangeex-message"></a>LB \_ SELITEMRANGEEX-Nachricht

Wählt mindestens ein aufeinander folgendes Element in einem Listenfeld mit mehrfacher Auswahl aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den nullbasierten Index des ersten auszuwählenden Elements an.

Windows 95/Windows 98/Windows Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Das bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Byte nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den nullbasierten Index des letzten auszuwählenden Elements an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, lautet der Rückgabewert LB \_ ERR.

## <a name="remarks"></a>Hinweise

Wenn der *wParam-Parameter* kleiner als der *lParam-Parameter* ist, wird der angegebene Elementbereich ausgewählt. Wenn *wParam* größer oder gleich *lParam* ist, wird der Bereich aus dem angegebenen Elementbereich entfernt. Um nur ein Element auszuwählen, wählen Sie zwei Elemente aus, und deaktivieren Sie dann das unerwünschte Element.

Verwenden Sie diese Meldung nur mit Listenfeldern mit mehrfacher Auswahl.

Diese Nachricht kann einen Bereich nur innerhalb der ersten 65.536 Elemente auswählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





