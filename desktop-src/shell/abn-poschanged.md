---
description: Benachrichtigt eine App-Leiste, wenn ein Ereignis aufgetreten ist, das sich auf die Größe und Position der App-Leiste auswirken kann.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: ABN_POSCHANGED (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92528de38b60c1f4705873427616b1ed7a5be6be5875a21e352d2136313c84df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943600"
---
# <a name="abn_poschanged-message"></a>ABN \_ POSCHANGED-Nachricht

Benachrichtigt eine App-Leiste, wenn ein Ereignis aufgetreten ist, das sich auf die Größe und Position der App-Leiste auswirken kann. Ereignisse umfassen Änderungen an Größe, Position und Sichtbarkeitszustand der Taskleiste sowie das Addition, Entfernen oder Ändern der Größe einer anderen App-Leiste auf derselben Seite des Bildschirms.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parameter

Diese Meldung enthält keine Parameter.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine App-Leiste sollte auf diese Benachrichtigung reagieren, indem die [**ABM \_ QUERYPOS-**](abm-querypos.md) und [**ABM \_ SETPOS-Nachrichten gesendet**](abm-setpos.md) werden. Wenn sich die Position geändert hat, sollte die App-Leiste die [**MoveWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-movewindow) aufrufen, um sich selbst an die neue Position zu verschieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

