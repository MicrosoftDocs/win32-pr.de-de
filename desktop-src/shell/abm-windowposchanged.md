---
description: Benachrichtigt das System, wenn sich die Position einer appbar geändert hat. Eine appbar sollte diese Meldung als Antwort auf die WM- \_ windowposchge-Nachricht anrufen.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: ABM_WINDOWPOSCHANGED Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484395"
---
# <a name="abm_windowposchanged-message"></a>ABM \_ windowposchge-Nachricht

Benachrichtigt das System, wenn sich die Position einer appbar geändert hat. Eine appbar sollte diese Meldung als Antwort auf die [**WM- \_ windowposchge**](/windows/desktop/winmsg/wm-windowposchanged) -Nachricht anrufen.


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die die zu aktivierende appbar identifiziert. Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird ignoriert, wenn der **HWND** -Member der Struktur, auf die von der *pabd* verwiesen wird, eine appbar zum automatischen Ausblenden identifiziert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

