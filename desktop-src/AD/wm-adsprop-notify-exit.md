---
title: WM_ADSPROP_NOTIFY_EXIT-Nachricht (Adsprop.h)
description: Eine Active Directory-Eigenschaftenblatterweiterung sendet die WM \_ ADSPROP \_ NOTIFY \_ EXIT-Nachricht an das Benachrichtigungsobjekt, wenn das Benachrichtigungsobjekt nicht mehr benötigt wird.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT-Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e144bb0b24112cabe1a806d4c746aac07708443665c0f457df8756be36d80b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181964"
---
# <a name="wm_adsprop_notify_exit-message"></a>WM \_ ADSPROP \_ NOTIFY \_ EXIT-Nachricht

Eine Active Directory-Eigenschaftenblatterweiterung sendet die **WM \_ ADSPROP \_ NOTIFY \_ EXIT-Nachricht** an das Benachrichtigungsobjekt, wenn das Benachrichtigungsobjekt nicht mehr benötigt wird.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Das Handle des Benachrichtigungsobjekts. Rufen Sie [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf, um dieses Handle abzurufen.

</dd> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Das Benachrichtigungsobjekt löscht sich selbst als Antwort auf diese Meldung. Wenn diese Nachricht gesendet wurde, sollte das Handle des Benachrichtigungsobjekts als ungültig betrachtet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Nachrichten in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





