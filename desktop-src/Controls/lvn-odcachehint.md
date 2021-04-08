---
title: LVN_ODCACHEHINT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem virtuellen Listenansicht-Steuerelement gesendet, wenn sich der Inhalt des Anzeige Bereichs geändert hat.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- Windows-Steuerelemente für LVN_ODCACHEHINT Benachrichtigungs
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
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957258"
---
# <a name="lvn_odcachehint-notification-code"></a>LVN \_ odcachehint-Benachrichtigungs Code

Wird von einem virtuellen Listenansicht-Steuerelement gesendet, wenn sich der Inhalt des Anzeige Bereichs geändert hat. Beispielsweise sendet ein Listenansicht-Steuerelement diesen Benachrichtigungs Code, wenn der Benutzer in der Anzeige des Steuer Elements einen Bildlauf durchführt. Der LVN \_ odcachehint-Benachrichtigungs Code wird in Form einer [**WM- \_**](wm-notify.md) Benachrichtigungs Meldung gesendet.


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmlvcachehint**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) -Struktur, die Informationen über den Bereich von Elementen enthält, die zwischengespeichert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungs Code empfängt, muss NULL zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Meldung verarbeiten, kann die Anwendung die im Cache gespeicherten Element Informationen aktualisieren, damit Sie beim Senden eines [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Codes sofort verfügbar ist.

Beachten Sie, dass es sich bei diesem Benachrichtigungs Code nicht immer um eine exakte Darstellung der Elemente handelt, die von [LVN \_ getdispinfo](lvn-getdispinfo.md)angefordert werden. Wenn das angeforderte Element bei der Behandlung von LVN getdispinfo nicht zwischengespeichert wird \_ , muss die Anwendung daher darauf vorbereitet sein, die angeforderten Informationen aus einer Quelle außerhalb des Caches bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





