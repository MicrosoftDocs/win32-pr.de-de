---
description: Eine Anwendung sendet die WM- \_ mdigetactive-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das Handle für das aktive untergeordnete MDI-Fenster abzurufen.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: WM_MDIGETACTIVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373167"
---
# <a name="wm_mdigetactive-message"></a>WM- \_ mdigetactive-Meldung

Eine Anwendung sendet die **WM- \_ mdigetactive** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das Handle für das aktive untergeordnete MDI-Fenster abzurufen.


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

Der maximierte Zustand. Wenn dieser Parameter nicht **null** ist, handelt es sich um einen Zeiger auf einen Wert, der den maximierten Zustand des untergeordneten MDI-Fensters angibt. Wenn der Wert **true** ist, wird das Fenster maximiert. der Wert **false** gibt an, dass dies nicht der Fall ist. Wenn dieser Parameter **null** ist, wird der-Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HWND**

Der Rückgabewert ist das Handle des aktiven untergeordneten MDI-Fensters.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




