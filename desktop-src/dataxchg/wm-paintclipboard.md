---
title: WM_PAINTCLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ -Besitzer Anzeige Format enthält und der Client Bereich der Zwischenablage-Viewer neu gezeichnet werden muss.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339324"
---
# <a name="wm_paintclipboard-message"></a>WM- \_ paintclipboard-Meldung

Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) Format enthält und der Client Bereich der Zwischenablage-Viewer neu gezeichnet werden muss.


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster der Zwischenablage Anzeige.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für ein globales Speicher Objekt, das eine [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur enthält. Die-Struktur definiert den zu zeichnenden Teil des Client Bereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Um zu ermitteln, ob der gesamte Client Bereich oder nur ein Teil davon neu gezeichnet werden muss, muss der Besitzer der Zwischenablage die Dimensionen des Zeichnungs Bereichs im **rcpaint** -Member von [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) mit den Dimensionen vergleichen, die in der letzten [**WM- \_ sizeclipboard**](wm-sizeclipboard.md) -Meldung angegeben sind.

Der Besitzer der Zwischenablage muss die [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) -Funktion verwenden, um den Arbeitsspeicher zu sperren, der die [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur enthält. Vor der Rückgabe muss der Besitzer der Zwischenablage diesen Speicher mithilfe der [**globalunlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) -Funktion entsperren.

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

[**WM- \_ sizeclipboard**](wm-sizeclipboard.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

