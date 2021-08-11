---
title: WM_ADSPROP_NOTIFY_PAGEHWND Meldung (Adsprop.h)
description: Eine Eigenschaftenblatterweiterung des Active Directory-Verzeichnisdiensts ruft den ADsPropSetHwnd auf, um das Benachrichtigungsobjekt über das Handle des Eigenschaftenseitenfensters zu informieren.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND-Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2835b4e0ff878b4c747f8c34b983beb3d66c550008a82ecadb2e5a23667abc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181731"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>WM \_ ADSPROP \_ NOTIFY \_ PAGEHWND-Nachricht

Eine Eigenschaftenblatterweiterung des Active Directory-Verzeichnisdiensts ruft den [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) auf, um das Benachrichtigungsobjekt über das Handle des Eigenschaftenseitenfensters zu informieren. Die **ADsPropSetHwnd-Funktion** sendet die **WM \_ ADSPROP NOTIFY \_ \_ PAGEHWND-Nachricht** an das Benachrichtigungsobjekt, das das Benachrichtigungsobjekt über das Handle des Eigenschaftenseitenfensters informiert.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

Das Handle des Benachrichtigungsobjekts. Rufen Sie [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf, um dieses Handle abzurufen.

</dd> <dt>

*hPage* 
</dt> <dd>

Ein Fensterhandle der Eigenschaftenseite.

</dd> <dt>

*ptzTitle* 
</dt> <dd>

Zeiger auf einen mit NULL endenden **WCHAR-Puffer,** der den Titel der Eigenschaftenseite enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Eine Active Directory-Eigenschaftenblatterweiterung ruft normalerweise die [**ADsPropSetHwnd-Funktion**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) auf, während die [**WM \_ INITDIALOG-Nachricht**](../dlgbox/wm-initdialog.md) verarbeitet wird.

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

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

