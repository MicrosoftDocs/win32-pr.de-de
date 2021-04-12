---
title: WM_ADSPROP_NOTIFY_PAGEHWND Meldung (adsprop. h)
description: Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung ruft das adspropsethwnd auf, um das Benachrichtigungs Objekt des Fenster Handles der Eigenschaften Seite zu informieren.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND Meldung Active Directory
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
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105615"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>"WM \_ adsprop"- \_ Benachrichtigungs \_ Meldung Benachrichtigen

Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung ruft das [**adspropsethwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) auf, um das Benachrichtigungs Objekt des Fenster Handles der Eigenschaften Seite zu informieren. Die **adspropsethwnd** -Funktion sendet die " **WM \_ adsprop \_ Notify \_ pagehwnd** "-Nachricht an das Benachrichtigungs Objekt, das das Benachrichtigungs Objekt des Fenster Handles der Eigenschaften Seite informiert.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hnotifyobj* 
</dt> <dd>

Das Handle des Benachrichtigungs Objekts. Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.

</dd> <dt>

*hPage* 
</dt> <dd>

Ein Fenster Handle der Eigenschaften Seite.

</dd> <dt>

*ptztitle* 
</dt> <dd>

Ein Zeiger auf einen null-terminierten **WCHAR** -Puffer, der den Titel der Eigenschaften Seite enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Eine Active Directory Eigenschaften Blatt Erweiterung ruft bei der Verarbeitung der [**WM- \_ InitDialog**](../dlgbox/wm-initdialog.md) -Nachricht normalerweise die Funktion [**adspropabthwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) auf.

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

[**Adspropsetup**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**Adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**WM \_ InitDialog**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

