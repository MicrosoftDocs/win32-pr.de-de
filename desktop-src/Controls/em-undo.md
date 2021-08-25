---
title: EM_UNDO Meldung (Winuser.h)
description: Diese Meldung rückgängigt den letzten Bearbeitungssteuerelementvorgang in der Rückgängig-Warteschlange des Steuerelements. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d82e6d0685314a79f1f95cff487ee3f52e2d1b70925c3e6e72f9263f442e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047920"
---
# <a name="em_undo-message"></a>EM \_ UNDO-Nachricht

Diese Meldung rückgängigt den letzten Bearbeitungssteuerelementvorgang in der Rückgängig-Warteschlange des Steuerelements. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

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

Für ein einzeiliges Bearbeitungssteuerelement ist der Rückgabewert immer **TRUE.**

Bei einem mehrzeiligen Bearbeitungssteuerelement ist der Rückgabewert **TRUE,** wenn der Rückgängig-Vorgang erfolgreich ist, oder **FALSE,** wenn der Rückgängig-Vorgang fehlschlägt.

## <a name="remarks"></a>Hinweise

**Steuerelemente bearbeiten und Rich Edit 1.0:** Ein Rückgängig-Vorgang kann ebenfalls rückgängig sein. Beispielsweise können Sie gelöschten Text mit der ersten **\_ EM-UNDO-Nachricht** wiederherstellen und den Text mit einer zweiten **\_ EM-UNDO-Nachricht** wieder entfernen, solange kein eingreifender Bearbeitungsvorgang erfolgt.

**Rich Edit 2.0 und höher:** Das Rückgängig-Feature ist auf mehreren Ebenen, sodass beim Senden von zwei **\_ EM-UNDO-Nachrichten** die letzten beiden Vorgänge in der Rückgängig-Warteschlange rückgängig werden. Um einen Vorgang zu wiederholen, senden Sie die [**\_ EM-REDO-Nachricht.**](em-redo.md)

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> </dl>

 

 





