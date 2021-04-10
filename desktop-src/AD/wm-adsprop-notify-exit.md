---
title: WM_ADSPROP_NOTIFY_EXIT Meldung (adsprop. h)
description: Eine Active Directory-Eigenschafts Blatt Erweiterung sendet die WM-Benachrichtigung zum \_ \_ Benachrichtigen der \_ Nachricht an das Benachrichtigungs Objekt, wenn das Benachrichtigungs Objekt nicht mehr benötigt wird.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT Meldung Active Directory
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
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957012"
---
# <a name="wm_adsprop_notify_exit-message"></a>WM \_ adsprop \_ Notify \_ Exit Message

Eine Active Directory-Eigenschafts Blatt Erweiterung sendet die WM-Benachrichtigung zum **\_ \_ Benachrichtigen \_** der Nachricht an das Benachrichtigungs Objekt, wenn das Benachrichtigungs Objekt nicht mehr benötigt wird.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Das Handle des Benachrichtigungs Objekts. Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.

</dd> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Das Benachrichtigungs Objekt wird als Antwort auf diese Nachricht gelöscht. Wenn diese Nachricht gesendet wurde, sollte das Benachrichtigungs Objekt Handle als ungültig betrachtet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Nachrichten in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





