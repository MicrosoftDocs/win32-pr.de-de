---
description: Eine Anwendung sendet die WM- \_ mdisetmenu-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das gesamte Menü eines MDI-Rahmen Fensters zu ersetzen, um das Fenstermenü des Rahmen Fensters oder beides zu ersetzen.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: WM_MDISETMENU Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368756"
---
# <a name="wm_mdisetmenu-message"></a>WM- \_ mdisetmenu-Meldung

Eine Anwendung sendet die **WM- \_ mdisetmenu** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das gesamte Menü eines MDI-Rahmen Fensters zu ersetzen, um das Fenstermenü des Rahmen Fensters oder beides zu ersetzen.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das neue Rahmen Fenstermenü. Wenn dieser Parameter **null** ist, wird das Menü Rahmen Fenster nicht geändert.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das neue Fenstermenü. Wenn dieser Parameter **null** ist, wird das Menü Fenster nicht geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HMENU**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das alte Rahmen Fenstermenü.

Wenn die Meldung fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Nach dem Senden dieser Nachricht muss eine Anwendung die [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) -Funktion zum Aktualisieren der Menüleiste aufruft.

Wenn diese Meldung das Fenstermenü ersetzt, werden die Menü Elemente des untergeordneten MDI-Fensters aus dem vorherigen Fenstermenü entfernt und dem Menü neues Fenster hinzugefügt.

Wenn ein untergeordnetes MDI-Fenster maximiert ist und diese Meldung das MDI-Frame Fenster-Menü ersetzt, werden das Fenstermenü Symbol und das Wiederherstellungs Symbol aus dem vorherigen Menü Fenster des Frames entfernt und dem Menü neues Rahmen Fenster hinzugefügt.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM- \_ mumgeleitet-freshmenu**](wm-mdirefreshmenu.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 
