---
title: WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop.h)
description: Eine Active Directory-Eigenschaftenblatterweiterung ruft die ADsPropGetInitInfo auf, um Daten über das Verzeichnisobjekt zu erhalten, für das die Eigenschaftenblatterweiterung gilt.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT Active Directory-Nachricht
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcad6ed359edf195b2355920b08d6010597f33dbc0f4e3b1e4c2438c3841ca47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024208"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>WM \_ ADSPROP \_ NOTIFY \_ PAGEINIT-Meldung

Eine Active Directory-Eigenschaftenblatterweiterung ruft [**die ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) auf, um Daten über das Verzeichnisobjekt zu erhalten, für das die Eigenschaftenblatterweiterung gilt. Die **ADsPropGetInitInfo-Funktion** sendet die **WM \_ ADSPROP NOTIFY \_ \_ PAGEINIT-Nachricht** an das Benachrichtigungsobjekt, um dieses Ergebnis zu erzielen.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle des Benachrichtigungsobjekts. Dies ist der *hNotifyObject-Parameter,* der durch einen Aufruf von [**ADsPropCreateNotifyObj erhalten wurde.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)

</dd> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

Zeiger auf eine [**ADSPROPINITPARAMS-Struktur,**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) die die Verzeichnisobjektinformationen empfängt. Dies ist der *pInitParams-Parameter,* der an [**ADsPropCreateNotifyObj übergeben wird.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung hat keinen Rückgabewert.

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

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





