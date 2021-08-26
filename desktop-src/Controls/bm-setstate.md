---
title: BM_SETSTATE (Winuser.h)
description: Legt den Hervorhebungszustand einer Schaltfläche fest. Der Hervorhebungszustand gibt an, ob die Schaltfläche so hervorgehoben ist, als hätte der Benutzer sie gedrückt. Sie können diese Nachricht explizit senden oder das Button \_ SetState-Makro verwenden.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3bb9451041c602541f039afcd85a895af2f02302dc5d55d64fbefb5bc6e3ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921210"
---
# <a name="bm_setstate-message"></a>BM \_ SETSTATE-Nachricht

Legt den Hervorhebungszustand einer Schaltfläche fest. Der Hervorhebungszustand gibt an, ob die Schaltfläche so hervorgehoben ist, als hätte der Benutzer sie gedrückt. Sie können diese Nachricht explizit senden oder das [**Button \_ SetState-Makro**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine **BOOL,** die angibt, ob die Schaltfläche hervorgehoben ist. Der Wert **TRUE hebt** die Schaltfläche hervor. Durch den Wert **FALSE werden** alle Hervorhebungen entfernt.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die Hervorhebung wirkt sich nur auf die Darstellung einer Schaltfläche aus. Dies hat keine Auswirkungen auf den Überprüfungszustand eines Optionsfelds oder Kontrollkästchens.

Eine Schaltfläche wird automatisch hervorgehoben, wenn der Benutzer den Cursor darüber positioniert und die linke Maustaste drückt und hält. Die Hervorhebung wird entfernt, wenn der Benutzer die Maustaste loslässt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





