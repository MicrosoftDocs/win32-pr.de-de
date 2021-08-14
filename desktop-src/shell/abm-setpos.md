---
description: Legt die Größe und Bildschirmposition einer App-Leiste fest.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: ABM_SETPOS (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861602"
---
# <a name="abm_setpos-message"></a>ABM \_ SETPOS-Nachricht

Legt die Größe und Bildschirmposition einer App-Leiste fest. Die Meldung gibt einen Bildschirmrand und das umrandende Rechteck für die App-Leiste an. Das System kann das umgebundene Rechteck so anpassen, dass die App-Leiste die Windows oder andere Appbars nicht beeinträchtigt.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Das **uEdge-Element** gibt einen Bildschirmrand an, und der **rc-Member** enthält das umrandende Rechteck. Wenn die [**SHAppBarMessage-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) zurückgegeben wird, **enthält rc** das genehmigte umgebundene Rechteck. Sie müssen beim Senden dieser Nachricht **die Member cbSize,** **hWnd,** **uEdge** und **rc** angeben. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Diese Meldung bewirkt, dass das System die [**ABN \_ POSCHANGED-Benachrichtigungsnachricht**](abn-poschanged.md) an alle App-Leisten sendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




