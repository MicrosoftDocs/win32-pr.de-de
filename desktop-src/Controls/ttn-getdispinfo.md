---
title: TTN_GETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Wird von einem QuickInfo-Steuerelement gesendet, um Informationen abzurufen, die zum Anzeigen eines QuickInfo-Fensters erforderlich sind. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29df1da7643384233b25af6a6efd99930d5b49d0b47b5ffead335b2307bd3de3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967810"
---
# <a name="ttn_getdispinfo-notification-code"></a>TTN \_ GETDISPINFO-Benachrichtigungscode

Wird von einem QuickInfo-Steuerelement gesendet, um Informationen abzurufen, die zum Anzeigen eines QuickInfo-Fensters erforderlich sind. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTTDISPINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) die das Tool identifiziert, das Text benötigt und die angeforderten Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das QuickInfo-Steuerelement zurück zu geben. Wenn ihr Meldungshandler das **uFlags-Element** der [**NMTTDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) auf TTF DI SETITEM festgelegt hat, speichert das QuickInfo-Steuerelement die Informationen und fordert sie \_ \_ nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTN \_ GETDISPINFOW** (Unicode) und **TTN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





