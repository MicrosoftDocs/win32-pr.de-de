---
title: WM_RENDERFORMAT Meldung (Winuser. h)
description: Wird an den Besitzer der Zwischenablage gesendet, wenn er das Rendern eines bestimmten Zwischenablage Formats verzögert hat und eine Anwendung Daten in diesem Format angefordert hat.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT Nachrichten Datenaustausch
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
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340708"
---
# <a name="wm_renderformat-message"></a>WM- \_ Renderformat-Meldung

Wird an den Besitzer der Zwischenablage gesendet, wenn er das Rendern eines bestimmten Zwischenablage Formats verzögert hat und eine Anwendung Daten in diesem Format angefordert hat. Der Besitzer der Zwischenablage muss die Daten im angegebenen Format Renderingdaten in der Zwischenablage platzieren, indem er die [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion aufruft.


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das zu rendernde [Zwischenablage Format](standard-clipboard-formats.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Bei der Reaktion auf eine **WM- \_ Renderformat** -Nachricht darf der Besitzer der Zwischenablage die Zwischenablage vor dem Aufrufen von [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)nicht öffnen. Das Öffnen der Zwischenablage ist nicht erforderlich, bevor Daten als Antwort auf **WM \_ Renderformat** platziert werden, und jeder Versuch, die Zwischenablage zu öffnen, schlägt fehl, da die Zwischenablage derzeit von der Anwendung geöffnet wird, die das zu rendernde Format angefordert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM- \_ renderallformats**](wm-renderallformats.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

 





