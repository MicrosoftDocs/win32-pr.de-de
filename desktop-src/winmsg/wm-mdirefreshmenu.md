---
description: Eine Anwendung sendet die \_ WM-MDMAKERFRESHMENU-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um das Fenstermenü des MDI-Rahmenfensters zu aktualisieren.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: WM_MDIREFRESHMENU-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 707059d3cc51703819968f929f9692dbb2422ee3f9fa77e2edb697f12257faf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200066"
---
# <a name="wm_mdirefreshmenu-message"></a>WM \_ MD JRFRESHMENU-Nachricht

Eine Anwendung sendet die **\_ WM-MDMAKERFRESHMENU-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um das Fenstermenü des MDI-Rahmenfensters zu aktualisieren.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HMENU**

Wenn die Meldung erfolgreich ist, ist der Rückgabewert das Handle für das Rahmenfenstermenü.

Wenn die Nachricht fehlschlägt, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Nach dem Senden dieser Nachricht muss eine Anwendung die [**DrawMenuBar-Funktion**](/windows/win32/api/winuser/nf-winuser-drawmenubar) aufrufen, um die Menüleiste zu aktualisieren.

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

[**WM \_ MDISETMENU**](wm-mdisetmenu.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schnittstelle für mehrere Dokumente](multiple-document-interface.md)
</dt> </dl>

 

 
