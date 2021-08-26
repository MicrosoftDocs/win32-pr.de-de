---
title: TTN_NEEDTEXT Benachrichtigungscode (Commctrl.h)
description: Wird von einem QuickInfo-Steuerelement gesendet, um Informationen abzurufen, die zum Anzeigen eines QuickInfo-Fensters erforderlich sind. Dieser Benachrichtigungscode ist identisch mit TTN \_ GETDISPINFO. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dae1ac1eb721d918acf38745f19c7e6dee4a6a296c7fa8003f516717ece6cf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967800"
---
# <a name="ttn_needtext-notification-code"></a>TTN \_ NEEDTEXT-Benachrichtigungscode

Wird von einem QuickInfo-Steuerelement gesendet, um Informationen abzurufen, die zum Anzeigen eines QuickInfo-Fensters erforderlich sind. Dieser Benachrichtigungscode ist identisch mit [TTN \_ GETDISPINFO](ttn-getdispinfo.md). Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TTN_NEEDTEXT

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

Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das QuickInfo-Steuerelement zurückzugeben. Wenn Ihr Nachrichtenhandler den **uFlags-Member** der [**NMTTDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) auf TTF \_ DI \_ SETITEM festlegt, speichert das QuickInfo-Steuerelement die Informationen und fordert sie nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTN \_ NEEDTEXTW** (Unicode) und **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





