---
title: WM_RENDERFORMAT (Winuser.h)
description: Wird an den Besitzer der Zwischenablage gesendet, wenn das Rendering eines bestimmten Zwischenablageformats verzögert wurde und eine Anwendung Daten in diesem Format angefordert hat.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT-Nachricht Data Exchange
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2885e056577656d6cabb8ea78f48a02a19f3c3c40bb3c30b1e5ca25c72cdf39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545309"
---
# <a name="wm_renderformat-message"></a>WM \_ RENDERFORMAT-Meldung

Wird an den Besitzer der Zwischenablage gesendet, wenn das Rendering eines bestimmten Zwischenablageformats verzögert wurde und eine Anwendung Daten in diesem Format angefordert hat. Der Besitzer der Zwischenablage muss Daten im angegebenen Format rendern und durch Aufrufen der [**Funktion SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) in der Zwischenablage platzieren.


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [Format der Zwischenablage,](standard-clipboard-formats.md) das gerendert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn der Besitzer der Zwischenablage auf eine **WM \_ RENDERFORMAT-Meldung** reagiert, darf er die Zwischenablage nicht öffnen, bevor [**er SetClipboardData aufruft.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) Das Öffnen der Zwischenablage ist vor dem Platzieren von Daten als Reaktion auf **WM \_ RENDERFORMAT** nicht erforderlich. Bei jedem Versuch, die Zwischenablage zu öffnen, wird ein Fehler angezeigt, da die Zwischenablage derzeit von der Anwendung geöffnet gehalten wird, die das zu rendernde Format angefordert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERALLFORMATS**](wm-renderallformats.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

 





