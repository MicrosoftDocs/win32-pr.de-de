---
title: WM_ADSPROP_NOTIFY_PAGEINIT Meldung (adsprop. h)
description: Eine Active Directory Eigenschaften Blatt Erweiterung ruft adspropgetinitinfo auf, um Daten über das Verzeichnis Objekt zu erhalten, für das die Eigenschaften Blatt Erweiterung gilt.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT Meldung Active Directory
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
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517600"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>WM \_ adsprop \_ benachrichtigt \_ pageInit-Nachricht

Eine Active Directory Eigenschaften Blatt Erweiterung ruft [**adspropgetinitinfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) auf, um Daten über das Verzeichnis Objekt zu erhalten, für das die Eigenschaften Blatt Erweiterung gilt. Die **adspropgetinitinfo** -Funktion sendet die " **WM \_ adsprop \_ Notify \_ pageInit** "-Nachricht an das Benachrichtigungs Objekt, um dieses Ergebnis zu erzielen.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle des Benachrichtigungs Objekts. Dies ist der *hnotifyobject* -Parameter, der durch einen Aufrufen von [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)abgerufen wird.

</dd> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*padspropinitparametriams* 
</dt> <dd>

Ein Zeiger auf eine [**adspropinitparameams**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) -Struktur, die die Verzeichnis Objektinformationen empfängt. Dies ist der an [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)übergebenen *pinitparameams* -Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Nachrichten in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**Adspropgetinitinfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**Adspropinitparameams**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





