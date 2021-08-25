---
title: EM_CANUNDO Meldung (Winuser.h)
description: Bestimmt, ob aktionen in der Rückgängig-Warteschlange eines Bearbeitungssteuerelements vorhanden sind. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 7b1cb56b07232c6b55a85b7387cf7b2fafd40ac29e5dc0520b45e1aa50cadcb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915990"
---
# <a name="em_canundo-message"></a>EM \_ CANUNDO-Nachricht

Bestimmt, ob aktionen in der Rückgängig-Warteschlange eines Bearbeitungssteuerelements vorhanden sind. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

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

Wenn aktionen in der Rückgängig-Warteschlange des Steuerelements vorhanden sind, ist der Rückgabewert ungleich 0 (null).

Wenn die Rückgängigwarteschlange leer ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Wenn die Rückgängig-Warteschlange nicht leer ist, können Sie die [**\_ EM-RÜCKGÄNGIG-Nachricht**](em-undo.md) an das Steuerelement senden, um den letzten Vorgang rückgängig zu machen.

**Steuerelemente bearbeiten und Rich Edit 1.0:** Die Rückgängig-Warteschlange enthält nur den letzten Vorgang.

**Rich Edit 2.0 und höher:** Die Rückgängig-Warteschlange kann mehrere Vorgänge enthalten.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





