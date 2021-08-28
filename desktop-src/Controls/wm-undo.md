---
title: WM_UNDO (Winuser.h)
description: Eine Anwendung sendet eine WM \_ UNDO-Nachricht an ein Bearbeitungssteuerteil, um den letzten Vorgang rückgängig zu machen. Wenn diese Meldung an ein Bearbeitungssteuerfeld gesendet wird, wird der zuvor gelöschte Text wiederhergestellt oder der zuvor hinzugefügte Text gelöscht.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO message Windows Controls
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6e4bd0715b7eeb5f99f34f5142ac3198c5c1eae53cf4486c3efce9dace19a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311340"
---
# <a name="wm_undo-message"></a>WM \_ UNDO-Meldung

Eine Anwendung sendet eine **WM \_ UNDO-Nachricht** an ein Bearbeitungssteuerteil, um den letzten Vorgang rückgängig zu machen. Wenn diese Meldung an ein Bearbeitungssteuerfeld gesendet wird, wird der zuvor gelöschte Text wiederhergestellt oder der zuvor hinzugefügte Text gelöscht.

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

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Meldung fehlschlägt, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

**Umfangreiche Bearbeitung:** Es wird empfohlen, [**EM \_ UNDO**](em-undo.md) anstelle von **WM \_ UNDO zu verwenden.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ CLEAR**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**WM \_ COPY**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**WM \_ CUT**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**WM \_ PASTE**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

