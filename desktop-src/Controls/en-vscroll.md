---
title: EN_VSCROLL Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer auf die vertikale Scrollleiste eines Bearbeitungssteuerelements klickt oder wenn der Benutzer mit dem Mausrad über das Bearbeitungssteuerelement scrollt.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c716ecb36c0d27b445446a30eb0a026edf3fd88641f469e50daef1763cd6ca66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047380"
---
# <a name="en_vscroll-notification-code"></a>EN \_ VSCROLL-Benachrichtigungscode

Wird gesendet, wenn der Benutzer auf die vertikale Scrollleiste eines Bearbeitungssteuerelements klickt oder wenn der Benutzer mit dem Mausrad über das Bearbeitungssteuerelement scrollt. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command) Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungssteuerelements. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungssteuerelement.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Meldung wird für die folgenden Mausereignisse auf der vertikalen Bildlaufleiste gesendet: Klicken sie entweder auf die Pfeilschaltfläche oder zwischen der Pfeilschaltfläche und dem Daumen. Die Nachricht wird jedoch nicht gesendet, wenn Sie auf die Scrollleistenmaus selbst klicken. Die Meldung wird auch gesendet, wenn ein Tastaturereignis eine Änderung im Ansichtsbereich des Bearbeitungssteuerelements verursacht, z. B. durch Drücken von HOME, END, PAGE UP, PAGE DOWN, UP ARROW oder DOWN ARROW.

Das Mausrad ist eine Maus mit einem Mittelpunktrad, das scrollt. Weitere Informationen finden Sie unter "Das Mausrad" unter [Informationen zur Mauseingabe.](/windows/desktop/inputdev/about-mouse-input)

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Um EN \_ VSCROLL-Benachrichtigungscodes zu empfangen, geben Sie [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

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

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwenden von Bearbeitungssteuerelementen](using-edit-controls.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

