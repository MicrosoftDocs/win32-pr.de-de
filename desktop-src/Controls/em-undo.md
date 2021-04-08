---
title: EM_UNDO Meldung (Winuser. h)
description: Diese Nachricht macht den letzten Bearbeitungs Steuerungs Vorgang in der Rückgängig-Warteschlange des-Steuer Elements rückgängig. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Windows-Steuerelemente für EM_UNDO Meldung
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
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741577"
---
# <a name="em_undo-message"></a>EM- \_ Rückgängig Meldung

Diese Nachricht macht den letzten Bearbeitungs Steuerungs Vorgang in der Rückgängig-Warteschlange des-Steuer Elements rückgängig. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Bei einem einzeiligen Bearbeitungs Steuerelement ist der Rückgabewert immer " **true**".

Bei einem mehrzeiligen Bearbeitungs Steuerelement ist der Rückgabewert **true** , wenn der Rückgängig-Vorgang erfolgreich ist, oder **false** , wenn der Rückgängig-Vorgang fehlschlägt.

## <a name="remarks"></a>Bemerkungen

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Ein Rückgängig-Vorgang kann auch rückgängig gemacht werden. Beispielsweise können Sie gelöschten Text mit der ersten **EM- \_ Rückgängig** -Nachricht wiederherstellen und den Text erneut mit einer zweiten **EM- \_ Rückgängig** -Meldung entfernen, solange es keinen dazwischen liegenden Bearbeitungsvorgang gibt.

**Rich Edit 2,0 und höher:** Die Rückgängig-Funktion ist eine mehrstufige Funktion, sodass das Senden von zwei **EM- \_ Rückgängig** -Nachrichten die letzten beiden Vorgänge in der rückgängig- Um einen Vorgang wiederholen, senden Sie die EM-Wiederholungs Nachricht. [**\_**](em-redo.md)

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ CanUndo**](em-canundo.md)
</dt> </dl>

 

 





