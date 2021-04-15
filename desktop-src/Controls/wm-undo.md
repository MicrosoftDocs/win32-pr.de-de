---
title: WM_UNDO Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM- \_ Rückgängig Meldung an ein Bearbeitungs Steuerelement, um den letzten Vorgang rückgängig zu machen. Wenn diese Nachricht an ein Bearbeitungs Steuerelement gesendet wird, wird der zuvor gelöschte Text wieder hergestellt oder der zuvor hinzugefügte Text gelöscht.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Windows-Steuerelemente für WM_UNDO Meldung
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
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477526"
---
# <a name="wm_undo-message"></a>WM- \_ Rückgängig Meldung

Eine Anwendung sendet eine **WM- \_ Rückgängig** Meldung an ein Bearbeitungs Steuerelement, um den letzten Vorgang rückgängig zu machen. Wenn diese Nachricht an ein Bearbeitungs Steuerelement gesendet wird, wird der zuvor gelöschte Text wieder hergestellt oder der zuvor hinzugefügte Text gelöscht.

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

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Meldung fehlschlägt, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Es wird empfohlen, [**EM \_ Undo**](em-undo.md) anstelle von **WM \_ Undo** zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ Clear**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**WM- \_ Kopie**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**WM \_ Ausschneiden**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**WM \_ Einfügen**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

