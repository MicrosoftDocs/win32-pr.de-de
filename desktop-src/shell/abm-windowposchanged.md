---
description: Benachrichtigt das System, wenn sich die Position einer Appbar geändert hat. Eine Appbar sollte diese Nachricht als Reaktion auf die WM \_ WINDOWPOSCHANGED-Nachricht aufrufen.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: ABM_WINDOWPOSCHANGED Meldung (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d770d50629342095308376856b98e6250adc1f9a1f2559da8509d685995428ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057810"
---
# <a name="abm_windowposchanged-message"></a>ABM \_ WINDOWPOSCHANGED-Meldung

Benachrichtigt das System, wenn sich die Position einer Appbar geändert hat. Eine Appbar sollte diese Nachricht als Reaktion auf die [**WM \_ WINDOWPOSCHANGED-Nachricht**](/windows/desktop/winmsg/wm-windowposchanged) aufrufen.


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) die die zu aktivierende Appbar identifiziert. Sie müssen die Member **cbSize** und **hWnd** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE** zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung wird ignoriert, wenn der **hWnd-Member** der -Struktur, auf die *pabd* zeigt, eine appbar für die automatische Benachrichtigung identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

