---
title: BM_SETSTATE Meldung (Winuser. h)
description: Legt den Hervorhebungs Zustand einer Schaltfläche fest. Der Hervorhebungs Zustand gibt an, ob die Schaltfläche hervorgehoben wird, als ob der Benutzer Sie gedrückt hätte. Sie können diese Nachricht explizit senden oder das SetState-Makro der Schaltfläche verwenden \_ .
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Windows-Steuerelemente für BM_SETSTATE Meldung
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
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339320"
---
# <a name="bm_setstate-message"></a>BM- \_ SetState-Nachricht

Legt den Hervorhebungs Zustand einer Schaltfläche fest. Der Hervorhebungs Zustand gibt an, ob die Schaltfläche hervorgehoben wird, als ob der Benutzer Sie gedrückt hätte. Sie können diese Nachricht explizit senden oder das [**\_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) -Makro der Schaltfläche verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **boolescher** Wert, der angibt, ob die Schaltfläche markiert ist. Durch den Wert **true** wird die Schaltfläche hervorgehoben. Der Wert **false** entfernt alle Hervorhebungen.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Die Hervorhebung wirkt sich nur auf die Darstellung einer Schaltfläche aus. Dies hat keine Auswirkung auf den Status des Kontrollkästchens oder des Kontrollkästchens.

Eine Schaltfläche wird automatisch hervorgehoben, wenn der Benutzer den Cursor darüber positioniert und die linke Maustaste gedrückt hält. Die Hervorhebung wird entfernt, wenn der Benutzer die Maustaste loslässt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**BM \_ GetState**](bm-getstate.md)
</dt> <dt>

[**BM- \_ setcheck**](bm-setcheck.md)
</dt> </dl>

 

 





