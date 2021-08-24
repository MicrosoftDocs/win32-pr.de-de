---
description: Eine Anwendung sendet die WM \_ MDISETMENU-Nachricht an ein Clientfenster mit mehreren Dokumenten (Multiple Document Interface, MDI), um das gesamte Menü eines MDI-Rahmenfensters, das Fenstermenü des Rahmenfensters oder beides zu ersetzen.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: WM_MDISETMENU-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fe87682691c5f113034c20c68cefd81ca3a7018bd44eb868c4f18551cacacd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772070"
---
# <a name="wm_mdisetmenu-message"></a>WM \_ MDISETMENU-Nachricht

Eine Anwendung sendet die **WM \_ MDISETMENU-Nachricht** an ein Clientfenster mit mehreren Dokumenten (Multiple Document Interface, MDI), um das gesamte Menü eines MDI-Rahmenfensters, das Fenstermenü des Rahmenfensters oder beides zu ersetzen.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das neue Rahmenfenstermenü. Wenn dieser Parameter **NULL** ist, wird das Rahmenfenstermenü nicht geändert.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das neue Fenstermenü. Wenn dieser Parameter **NULL** ist, wird das Fenstermenü nicht geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HMENU**

Wenn die Meldung erfolgreich ist, ist der Rückgabewert das Handle für das alte Framefenstermenü.

Wenn die Nachricht fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Nach dem Senden dieser Nachricht muss eine Anwendung die [**DrawMenuBar-Funktion**](/windows/win32/api/winuser/nf-winuser-drawmenubar) aufrufen, um die Menüleiste zu aktualisieren.

Wenn diese Meldung das Fenstermenü ersetzt, werden die Menüelemente des untergeordneten MDI-Fensters aus dem vorherigen Fenstermenü entfernt und dem neuen Fenstermenü hinzugefügt.

Wenn ein untergeordnetes MDI-Fenster maximiert ist und diese Meldung das MDI-Rahmenfenstermenü ersetzt, werden das Fenstermenüsymbol und das Wiederherstellungssymbol aus dem vorherigen Framefenstermenü entfernt und dem neuen Rahmenfenstermenü hinzugefügt.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ MD JRFRESHMENU**](wm-mdirefreshmenu.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schnittstelle für mehrere Dokumente](multiple-document-interface.md)
</dt> </dl>

 

 
