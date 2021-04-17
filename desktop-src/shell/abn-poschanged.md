---
description: Benachrichtigt eine appbar, wenn ein Ereignis aufgetreten ist, das sich auf die Größe und Position der appbar auswirken kann.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: ABN_POSCHANGED Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977425"
---
# <a name="abn_poschanged-message"></a>ABN- \_ Nachricht

Benachrichtigt eine appbar, wenn ein Ereignis aufgetreten ist, das sich auf die Größe und Position der appbar auswirken kann. Zu den Ereignissen zählen Änderungen in der Größe, Position und Sichtbarkeit der Taskleiste sowie das Hinzufügen, entfernen oder Ändern der Größe einer anderen appbar auf der gleichen Seite des Bildschirms.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parameter

Diese Nachricht weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine appbar sollte auf diese Benachrichtigungs Meldung reagieren, indem die [**ABM- \_ querypos**](abm-querypos.md) -und [**ABM- \_ SetPos**](abm-setpos.md) -Nachrichten gesendet werden. Wenn sich die Position geändert hat, sollte die appbar die [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) -Funktion zum Verschieben an die neue Position aufruft.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

