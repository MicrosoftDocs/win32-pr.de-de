---
title: LVN_ODCACHEHINT Benachrichtigungscode (Commctrl.h)
description: Wird von einem virtuellen Listenansichtssteuerelement gesendet, wenn sich der Inhalt des Anzeigebereichs geändert hat.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3693291eeaef0879bdf861f392b89a1d0f2d5ec52f8a9c0d092b5495eb4565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170177"
---
# <a name="lvn_odcachehint-notification-code"></a>LVN \_ ODCACHEHINT-Benachrichtigungscode

Wird von einem virtuellen Listenansichtssteuerelement gesendet, wenn sich der Inhalt des Anzeigebereichs geändert hat. Beispielsweise sendet ein Listenansicht-Steuerelement diesen Benachrichtigungscode, wenn der Benutzer die Anzeige des Steuerelements scrollt. Der LVN \_ ODCACHEHINT-Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVCACHEHINT-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) die Informationen zum Zwischenspeicherungsbereich von Elementen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode empfängt, muss 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Durch die Behandlung dieser Nachricht kann die Anwendung die im Cache gespeicherten Elementinformationen aktualisieren, sodass sie sofort verfügbar sind, wenn ein [LVN \_ GETDISPINFO-Benachrichtigungscode](lvn-getdispinfo.md) gesendet wird.

Beachten Sie, dass dieser Benachrichtigungscode nicht immer eine genaue Darstellung der Elemente ist, die von [LVN \_ GETDISPINFO](lvn-getdispinfo.md)angefordert werden. Wenn das angeforderte Element bei der Verarbeitung von LVN GETDISPINFO nicht zwischengespeichert \_ wird, muss die Anwendung daher darauf vorbereitet sein, die angeforderten Informationen von einer Quelle außerhalb des Caches anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





