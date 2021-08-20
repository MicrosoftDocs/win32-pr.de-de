---
title: PBM_SETRANGE Nachricht (Commctrl.h)
description: Legt die Minimal- und Höchstwerte für eine Statusanzeige fest und zeichnet die Leiste neu, um den neuen Bereich widerzuspiegeln.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5dca4e4be30b50627d8583a67801dc5cb246ef65e9cd267e6d7b3ee3ed7869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170197"
---
# <a name="pbm_setrange-message"></a>PBM \_ SETRANGE-Nachricht

Legt die Minimal- und Höchstwerte für eine Statusanzeige fest und zeichnet die Leiste neu, um den neuen Bereich widerzuspiegeln.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Minimalbereichswert an, und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den maximalen Bereichswert an. Der Mindestbereichswert darf nicht negativ sein. Standardmäßig ist der Mindestwert 0 (null). Der maximale Bereichswert muss größer als der Mindestbereichswert sein. Standardmäßig ist der maximale Bereichswert 100.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die vorherigen Bereichswerte zurück, andernfalls 0 (null). [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den vorherigen Mindestwert und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den vorherigen Höchstwert an.

## <a name="remarks"></a>Hinweise

Wenn Sie die Bereichswerte nicht festlegen, legt das System den Mindestwert auf 0 und den Höchstwert auf 100 fest. Da diese Nachricht den Bereich als 16-Bit-Ganzzahl ohne Vorzeichen ausdrückt, kann sie von 0 auf 65.535 erweitert werden. Der Mindestwert im Bereich kann zwischen 0 und 65.535 liegen. Ebenso kann der Höchstwert zwischen 0 und 65.535 sein.

Um einen größeren Bereich festzulegen, rufen Sie [**PBM \_ SETRANGE32**](pbm-setrange32.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**PBM \_ GETRANGE**](pbm-getrange.md)
</dt> <dt>

[**PBM \_ SETRANGE32**](pbm-setrange32.md)
</dt> </dl>

 

