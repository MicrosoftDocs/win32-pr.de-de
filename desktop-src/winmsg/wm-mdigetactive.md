---
description: Eine Anwendung sendet die WM MDIGETACTIVE-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um das Handle für das aktive untergeordnete \_ MDI-Fenster abzurufen.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: WM_MDIGETACTIVE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7716138028f7fe7447cc89d8feded7806f4f8757cd4a18b4bef6f2d812de3f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200140"
---
# <a name="wm_mdigetactive-message"></a>WM \_ MDIGETACTIVE-Nachricht

Eine Anwendung sendet die **WM \_ MDIGETACTIVE-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um das Handle für das aktive untergeordnete MDI-Fenster abzurufen.


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Der maximierte Zustand. Wenn dieser Parameter nicht **NULL ist,** ist er ein Zeiger auf einen Wert, der den maximierten Zustand des untergeordneten MDI-Fensters angibt. Wenn der Wert **TRUE ist,** wird das Fenster maximiert. Der Wert **FALSE gibt an,** dass dies nicht der Wert ist. Wenn dieser Parameter **NULL ist,** wird der -Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HWND**

Der Rückgabewert ist das Handle für das aktive untergeordnete MDI-Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über mehrere Dokumentschnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




