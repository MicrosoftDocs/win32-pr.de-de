---
title: EN_HSCROLL Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer auf die horizontale Scrollleiste eines Bearbeitungssteuerelements klickt. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine WM \_ COMMAND-Meldung. Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e5b0f42d08977f7a1be68a5010aa7403b10fc2e5a126aa542bb25a644a7b70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436770"
---
# <a name="en_hscroll-notification-code"></a>EN \_ HSCROLL-Benachrichtigungscode

Wird gesendet, wenn der Benutzer auf die horizontale Scrollleiste eines Bearbeitungssteuerelements klickt. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command) Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.


```C++
EN_HSCROLL

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

Dieser Benachrichtigungscode wird für die folgenden Mausereignisse auf der horizontalen Bildlaufleiste gesendet: Klicken sie entweder auf die Pfeilschaltfläche oder zwischen der Pfeilschaltfläche und dem Daumen. Der Benachrichtigungscode wird jedoch nicht gesendet, wenn Sie auf den Schiebeleistenfinger selbst klicken. Der Benachrichtigungscode wird auch gesendet, wenn ein Tastaturereignis eine Änderung im Ansichtsbereich des Bearbeitungssteuerelements verursacht, z. B. durch Drücken von HOME, END, LEFT ARROW oder RIGHT ARROW.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Um **EN \_ HSCROLL-Benachrichtigungscodes** zu empfangen, geben Sie [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[EN \_ VSCROLL](en-vscroll.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

