---
title: WM_ADSPROP_NOTIFY_ERROR Meldung (Adsprop.h)
description: Die WM \_ ADSPROP \_ NOTIFY \_ ERROR-Meldung fügt eine Fehlermeldung zu einer Liste von Fehlermeldungen hinzu, die durch Aufrufen der ADsPropShowErrorDialog-Funktion angezeigt werden.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR-Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52f88cd4c60dcfcceed60ca644f7c59f65bee16e344cc17664e8b4be1ee18fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024288"
---
# <a name="wm_adsprop_notify_error-message"></a>WM \_ ADSPROP \_ NOTIFY ERROR \_ MESSAGE

Die **WM \_ ADSPROP NOTIFY \_ \_ ERROR-Meldung** fügt eine Fehlermeldung zu einer Liste von Fehlermeldungen hinzu, die durch Aufrufen der [**ADsPropShowErrorDialog-Funktion**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) angezeigt werden.


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle des Benachrichtigungsobjekts. Dies ist der *hNotifyObject-Parameter,* der von [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)abgerufen wird.

</dd> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ADSPROPERROR-Struktur,**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) die Fehlermeldungsdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Die [**ADsPropSendErrorMessage-Funktion**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) ist die bevorzugte Methode zum Senden dieser Nachricht.

Die von der **WM \_ ADSPROP \_ NOTIFY \_ ERROR-Meldung** hinzugefügten Fehlermeldungen werden gesammelt, bis [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) aufgerufen wird. **ADsPropShowErrorDialog** kombiniert die gesammelten Fehlermeldungen und zeigt sie an. Wenn das Fehlerdialogfeld verworfen wird, werden die gesammelten Fehlermeldungen gelöscht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Nachrichten in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





