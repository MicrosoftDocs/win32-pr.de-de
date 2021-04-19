---
title: WM_ADSPROP_NOTIFY_APPLY Meldung (adsprop. h)
description: Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung sendet die WM- \_ adsprop \_ Notify \_ Apply-Meldung an das Benachrichtigungs Objekt, wenn die Eigenschaften Seite "PSN \_ Apply Handler" erfolgreich ist.
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
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345504"
---
# <a name="wm_adsprop_notify_apply-message"></a>"WM \_ adsprop \_ Notify \_ Apply Message"

Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung sendet die **WM- \_ adsprop \_ Notify \_ Apply** -Meldung an das Benachrichtigungs Objekt, wenn die Eigenschaften Seite "PSN \_ Apply Handler" erfolgreich ist.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

Beim Hinzufügen von Seiten zum MMC-Snap-in "Active Directory-Manager" erstellt Active Directory MMC-Eigenschaften Blätter die Benachrichtigungsobjekte durch einen Aufrufen der Funktion " [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) " und übergibt dann das Benachrichtigungs Objekt Handle an jede Eigenschaften Seite.

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

 

 





