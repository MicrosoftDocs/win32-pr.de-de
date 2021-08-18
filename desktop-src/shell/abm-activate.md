---
description: Benachrichtigt das System, dass eine App-Leiste aktiviert wurde. Eine App-Leiste sollte diese Nachricht als Antwort auf die WM \_ ACTIVATE-Nachricht aufrufen.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224f04a88a1e69a1a67fc08c6018d33af2bcdbc6f34ff9fbd00d1dd76f82ce5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461133"
---
# <a name="abm_activate-message"></a>ABM \_ ACTIVATE-Nachricht

Benachrichtigt das System, dass eine App-Leiste aktiviert wurde. Eine App-Leiste sollte diese Nachricht als Antwort auf die [**WM \_ ACTIVATE-Nachricht**](/windows/desktop/inputdev/wm-activate) aufrufen.


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) die die zu aktivierende App-Leiste identifiziert. Sie müssen beim Senden **dieser Nachricht die Member cbSize** und **hWnd** angeben. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Diese Meldung wird ignoriert, wenn der **hWnd-Member** der Struktur, auf die *pabd* zeigt, eine App-Leiste für die automatische Eindung identifiziert. Das System legt automatisch die Z-Reihenfolge für App-Leisten für die automatischeHide fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

