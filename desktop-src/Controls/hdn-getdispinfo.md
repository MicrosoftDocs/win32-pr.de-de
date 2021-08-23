---
title: HDN_GETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Wird an den Besitzer eines Headersteuerelements gesendet, wenn das Steuerelement Informationen zu einem Rückrufheaderelement benötigt. Dieser Benachrichtigungscode wird als WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6e6cbc9559cda3312ecdca341aa7c7ad2b44dc5cc29e50690ddf10b2729a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435450"
---
# <a name="hdn_getdispinfo-notification-code"></a>HDN \_ GETDISPINFO-Benachrichtigungscode

Wird an den Besitzer eines Headersteuerelements gesendet, wenn das Steuerelement Informationen zu einem Rückrufheaderelement benötigt. Dieser Benachrichtigungscode wird als [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) Bei der Eingabe geben die Felder der Struktur an, welche Informationen erforderlich sind und welches Element von Interesse ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein LRESULT zurück.

## <a name="remarks"></a>Hinweise

Füllen Sie die entsprechenden Member der -Struktur aus, um die angeforderten Informationen an das Headersteuerelement zurückzugeben. Wenn Ihr Nachrichtenhandler den **Maskenmember** der [**NMHDDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) auf HDI \_ DI \_ SETITEM festlegt, speichert das Headersteuerelement die Informationen und fordert sie nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDN \_ GETDISPINFOW** (Unicode) und **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





