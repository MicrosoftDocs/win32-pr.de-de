---
description: Benachrichtigt das System, dass eine appbar aktiviert wurde. Eine appbar sollte diese Meldung als Antwort auf die WM- \_ Aktivierungs Nachricht anrufen.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128481"
---
# <a name="abm_activate-message"></a>ABM- \_ Aktivierungs Nachricht

Benachrichtigt das System, dass eine appbar aktiviert wurde. Eine appbar sollte diese Meldung als Antwort auf die [**WM- \_ Aktivierungs**](/windows/desktop/inputdev/wm-activate) Nachricht anrufen.


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
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

Diese Meldung wird ignoriert, wenn der **HWND** -Member der Struktur, auf die von der *pabd* verwiesen wird, eine appbar zum automatischen Ausblenden identifiziert. Das System legt automatisch die z-Reihenfolge für automatische Ausblenden von appbars fest.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

