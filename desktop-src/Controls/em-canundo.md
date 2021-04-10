---
title: EM_CANUNDO Meldung (Winuser. h)
description: Bestimmt, ob in der Rückgängig-Warteschlange eines Bearbeitungs Steuer Elements Aktionen vorhanden sind. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Windows-Steuerelemente für EM_CANUNDO Meldung
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104504"
---
# <a name="em_canundo-message"></a>EM \_ CanUndo-Nachricht

Bestimmt, ob in der Rückgängig-Warteschlange eines Bearbeitungs Steuer Elements Aktionen vorhanden sind. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Wenn Aktionen in der Rückgängig-Warteschlange des Steuer Elements vorhanden sind, ist der Rückgabewert ungleich 0 (null).

Wenn die Rückgängig-Warteschlange leer ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn die Rückgängig-Warteschlange nicht leer ist, können Sie die [**EM- \_ Rückgängig**](em-undo.md) Meldung an das Steuerelement senden, um den letzten Vorgang rückgängig zu machen.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Die Rückgängig-Warteschlange enthält nur den letzten Vorgang.

**Rich Edit 2,0 und höher:** Die Rückgängig-Warteschlange kann mehrere Vorgänge enthalten.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> </dl>

 

 





