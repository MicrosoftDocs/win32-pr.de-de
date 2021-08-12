---
title: BM_SETSTYLE Meldung (Winuser.h)
description: Legt den Stil einer Schaltfläche fest. Sie können diese Nachricht explizit senden oder das Button \_ SetStyle-Makro verwenden.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674418"
---
# <a name="bm_setstyle-message"></a>BM \_ SETSTYLE-Nachricht

Legt den Stil einer Schaltfläche fest. Sie können diese Nachricht explizit senden oder das [**Button \_ SetStyle-Makro**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Schaltflächenformat. Dieser Parameter kann eine Kombination aus Schaltflächenstilen sein. Eine Tabelle mit Schaltflächenstilen finden Sie unter [Schaltflächenstile.](button-styles.md)

</dd> <dt>

*lParam* 
</dt> <dd>

[**LowORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) von *lParam* ist eine **BOOL,** die angibt, ob die Schaltfläche neu gezeichnet werden soll. Mit dem Wert **TRUE** wird die Schaltfläche neu gezeichnet. Der Wert **FALSE** hat die Schaltfläche nicht neu gezeichnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

