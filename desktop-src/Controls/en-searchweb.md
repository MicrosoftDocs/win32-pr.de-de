---
title: EN_SEARCHWEB Benachrichtigungscode (CommCtrl.h)
description: Wird gesendet, wenn ein Bearbeitungssteuerelement den Tastaturfokus verliert. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine WM \_ NOTIFY-Nachricht.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 606f53427426e4c9d20c2e4c12245569ed1d8a53ed7ea29162516f6d65fd1baa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047470"
---
# <a name="en_searchweb-notification-code"></a>EN \_ SEARCHWEB-Benachrichtigungscode

Wird gesendet, nachdem ein Bearbeitungssteuerelement eine Websuche durchgeführt hat, wenn das Feature "Web durchsuchen" aktiviert ist. Weitere Informationen finden Sie [unter EM_ENABLESEARCHWEB](em-enablesearchweb.md). Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Bearbeitungssteuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMSEARCHWEB-Struktur.**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





