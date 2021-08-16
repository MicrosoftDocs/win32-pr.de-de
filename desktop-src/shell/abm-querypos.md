---
description: Fordert eine Größe und Eine Bildschirmposition für eine App-Leiste an.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: ABM_QUERYPOS Meldung (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f7a5e78b6b040904144a64e1068fea3a3e56c7b42fdfcf314f2ced4bfff9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225031"
---
# <a name="abm_querypos-message"></a>ABM \_ QUERYPOS-Nachricht

Fordert eine Größe und Eine Bildschirmposition für eine App-Leiste an. Wenn die Anforderung erfolgt, schlägt die Nachricht einen Bildschirmrand und ein umschließendes Rechteck für die Appbar vor. Das System passt das umschließende Rechteck so an, dass die Appbar die Windows Taskleiste oder andere App-Leisten nicht beeinträchtigt.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Der **uEdge-Member** gibt einen Bildschirmrand an, und das **rc-Element** enthält das vorgeschlagene umgrenzende Rechteck. Wenn die [**SHAppBarMessage-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) zurückgegeben wird, enthält **rc** das genehmigte umschließende Rechteck. Sie müssen die Member **cbSize,** **hWnd,** **uEdge** und **rc** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE** zurück.

## <a name="remarks"></a>Hinweise

Eine Appbar sollte diese Nachricht senden, bevor die [**ABM \_ SETPOS-Nachricht**](abm-setpos.md) gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




