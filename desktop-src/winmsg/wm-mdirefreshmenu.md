---
description: Eine Anwendung sendet die WM- \_ mumgeleitet freshmenu-Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Fenstermenü des MDI-Rahmen Fensters zu aktualisieren.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: WM_MDIREFRESHMENU Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357766"
---
# <a name="wm_mdirefreshmenu-message"></a>WM- \_ mumgeleitet freshmenu-Meldung

Eine Anwendung sendet die **WM- \_ mumgeleitet freshmenu** -Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Fenstermenü des MDI-Rahmen Fensters zu aktualisieren.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HMENU**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das Rahmen Fenstermenü.

Wenn die Meldung fehlschlägt, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Nach dem Senden dieser Nachricht muss eine Anwendung die [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) -Funktion zum Aktualisieren der Menüleiste aufruft.

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

[**WM- \_ mdisetmenu**](wm-mdisetmenu.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 
