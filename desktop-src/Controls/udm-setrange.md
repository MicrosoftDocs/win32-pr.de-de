---
title: UDM_SETRANGE (Commctrl.h)
description: Legt die minimalen und maximalen Positionen (Bereich) für ein Auf-Ab-Steuerelement fest.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60499c960b7f2e496dc4317229865a8838013fc5d78c194072bee27e761ba4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408055"
---
# <a name="udm_setrange-message"></a>UDM \_ SETRANGE-Nachricht

Legt die minimalen und maximalen Positionen (Bereich) für ein Auf-Ab-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine **Kurzform,** die die maximale Position für das  Auf-Ab-Steuerelement angibt, und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist eine kurz, die die Mindestposition angibt. Keine der Beiden Position kann größer als der UD \_ MAXVAL-Wert oder kleiner als der UD \_ MINVAL-Wert sein. Darüber hinaus darf der Unterschied zwischen den beiden Positionen UD \_ MAXVAL nicht überschreiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die maximale Position kann kleiner als die minimale Position sein. Wenn Sie auf die Nach-oben-Schaltfläche klicken, wird die aktuelle Position näher an die maximale Position bewegt, und durch Klicken auf die Schaltfläche mit dem Pfeil nach unten wird die Minimale Position angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM \_ SETRANGE**](udm-setrange.md)
</dt> </dl>

 

