---
description: Eine Anwendung sendet die WM- \_ mdicreate-Meldung an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu erstellen.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: WM_MDICREATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362597"
---
# <a name="wm_mdicreate-message"></a>WM- \_ mdicreate-Meldung

Eine Anwendung sendet die **WM- \_ mdicreate** -Meldung an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu erstellen.


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur, die Informationen enthält, die das System verwendet, um das untergeordnete MDI-Fenster zu erstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HWND**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das neue untergeordnete Fenster.

Wenn die Meldung fehlschlägt, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Das untergeordnete MDI-Fenster wird mit [**den Fenster Stil**](window-styles.md) Bits **WS \_ Child**, **WS \_ clipcaption**, **WS \_ clipchildren**, **WS \_ sysmenu**, **WS \_ Caption**, **WS Thick \_ Frame**, **WS \_ MinimizeBox** und **WS \_ MaximizeBox** sowie zusätzlichen stilbits erstellt, die in der [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur angegeben sind. Das System fügt den Titel des neuen untergeordneten Fensters dem Fenstermenü des Rahmen Fensters hinzu. Eine Anwendung sollte diese Meldung verwenden, um alle untergeordneten Fenster des Client Fensters zu erstellen.

Wenn ein MDI-Client Fenster eine Nachricht empfängt, die die Aktivierung der untergeordneten Fenster ändert, während das aktive untergeordnete Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.

Wenn ein untergeordnetes MDI-Fenster erstellt wird, sendet das System die [**WM \_ Create**](wm-create.md) -Meldung an das Fenster. Der *LPARAM* -Parameter der " **WM \_ Create** "-Meldung enthält einen Zeiger auf eine " [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) "-Struktur. Der Member *lpkreateparameams* dieser Struktur enthält einen Zeiger auf die [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur, die mit der **WM- \_ mdicreate** -Meldung übergeben wurde, die das untergeordnete MDI-Fenster erstellt hat.

Eine Anwendung sollte keine zweite WM- **\_ mdicreate** -Nachricht senden, während eine **WM- \_ mdicreate** -Nachricht noch verarbeitet wird. Beispielsweise sollte eine **WM- \_ mdicreate** -Nachricht nicht gesendet werden, solange ein untergeordnetes MDI-Fenster die **WM- \_ mdicreate** -Nachricht verarbeitet.

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

[**"Anatemdiwindow"**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**Mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**WM \_ Erstellen**](wm-create.md)
</dt> <dt>

[**WM- \_ mdidestroy**](wm-mdidestroy.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 
