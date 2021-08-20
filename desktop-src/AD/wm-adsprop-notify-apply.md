---
title: WM_ADSPROP_NOTIFY_APPLY-Nachricht (Adsprop.h)
description: Eine Eigenschaftenblatterweiterung des Active Directory-Verzeichnisdiensts sendet die WM \_ ADSPROP \_ NOTIFY \_ APPLY-Meldung an das Benachrichtigungsobjekt, wenn der PSN APPLY-Handler der Eigenschaftenseite \_ erfolgreich ist.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cc130a83aa77021e0be512d9b2ad27914b4c6be382c0290e082e1fbd67b8b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024298"
---
# <a name="wm_adsprop_notify_apply-message"></a>WM \_ ADSPROP \_ NOTIFY \_ APPLY-Nachricht

Eine Eigenschaftenblatterweiterung des Active Directory-Verzeichnisdiensts sendet die **WM \_ ADSPROP \_ NOTIFY \_ APPLY-Meldung** an das Benachrichtigungsobjekt, wenn der PSN APPLY-Handler der Eigenschaftenseite \_ erfolgreich ist.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

Beim Hinzufügen von Seiten zum ACTIVE Directory Manager-MMC-Snap-In erstellen Active Directory MMC-Eigenschaftenblätter die Benachrichtigungsobjekte durch einen Aufruf der [**ADsPropCreateNotifyObj-Funktion**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) und übergeben dann das Handle des Benachrichtigungsobjekts an jede Eigenschaftenseite.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Nachrichten in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





