---
title: EM_EMPTYUNDOBUFFER-Nachricht (Winuser.h)
description: Setzt das Rückgängig-Flag eines Bearbeitungssteuerelements zurück. Das Rückgängig-Flag wird immer dann festgelegt, wenn ein Vorgang innerhalb des Bearbeitungssteuerelements rückgängig macht werden kann. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d59dab38bca921e2125377889f8d18ddf6eb45c023badeead47f7e07b860fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915900"
---
# <a name="em_emptyundobuffer-message"></a>EM \_ EMPTYUNDOBUFFER-Nachricht

Setzt das Rückgängig-Flag eines Bearbeitungssteuerelements zurück. Das Rückgängig-Flag wird immer dann festgelegt, wenn ein Vorgang innerhalb des Bearbeitungssteuerelements rückgängig macht werden kann. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

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

Das Rückgängig-Flag wird automatisch zurückgesetzt, wenn das Bearbeitungssteuerelement eine [**WM \_ SETTEXT-**](/windows/desktop/winmsg/wm-settext) oder [**EM \_ SETHANDLE-Nachricht**](em-sethandle.md) empfängt.

**Steuerelemente bearbeiten und Rich Edit 1.0:** Das Steuerelement kann den letzten Vorgang nur rückgängig machen oder wiederholen.

**Rich Edit 2.0 und höher:** Die **EM \_ EMPTYUNDOBUFFER-Nachricht** leert alle Rückgängig- und Wiederholungspuffer. Umfangreiche Bearbeitungssteuerelemente ermöglichen es dem Benutzer, mehrere Vorgänge rückgängig zu machen oder zu wiederholen.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

