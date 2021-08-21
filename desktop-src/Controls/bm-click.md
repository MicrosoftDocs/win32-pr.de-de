---
title: BM_CLICK Meldung (Winuser.h)
description: Simuliert das Klicken des Benutzers auf eine Schaltfläche. Diese Meldung bewirkt, dass die Schaltfläche die WM \_ LBUTTONDOWN- und WM \_ LBUTTONUP-Meldungen empfängt und das übergeordnete Fenster der Schaltfläche einen BN \_ CLICKED-Benachrichtigungscode empfängt.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fdf1e206546bcdb3fa0888276414bd44b927e96a8478be4ae8a5ce2d2a5169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674982"
---
# <a name="bm_click-message"></a>BM \_ CLICK-Nachricht

Simuliert das Klicken des Benutzers auf eine Schaltfläche. Diese Meldung bewirkt, dass die Schaltfläche die [**WM \_ LBUTTONDOWN-**](/windows/desktop/inputdev/wm-lbuttondown) und [**WM \_ LBUTTONUP-Meldungen**](/windows/desktop/inputdev/wm-lbuttonup) empfängt und das übergeordnete Fenster der Schaltfläche einen BN CLICKED-Benachrichtigungscode [ \_ empfängt.](bn-clicked.md)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn sich die Schaltfläche in einem Dialogfeld befindet und das Dialogfeld nicht aktiv ist, schlägt die **BM \_ CLICK-Meldung** möglicherweise fehl. Um in dieser Situation erfolgreich zu sein, rufen Sie die [**Funktion SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) auf, um das Dialogfeld zu aktivieren, bevor Sie die **\_ BM-CLICK-Nachricht** an die Schaltfläche senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

