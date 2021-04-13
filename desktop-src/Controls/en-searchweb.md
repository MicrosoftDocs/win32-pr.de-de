---
title: EN_SEARCHWEB Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus verliert. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM-Benachrichtigungs \_ Meldung.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- Windows-Steuerelemente für EN_SEARCHWEB Benachrichtigungs
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
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475387"
---
# <a name="en_searchweb-notification-code"></a>EN \_ Searchweb-Benachrichtigungs Code

Wird gesendet, nachdem ein Bearbeitungs Steuerelement eine Websuche durchgeführt hat, wenn das Feature "Web suchen" aktiviert ist. Weitere Informationen finden Sie unter [EM_ENABLESEARCHWEB](em-enablesearchweb.md). Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Bearbeitungs Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmsearchweb**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) -Struktur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ enablesearchweb**](em-enablesearchweb.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





