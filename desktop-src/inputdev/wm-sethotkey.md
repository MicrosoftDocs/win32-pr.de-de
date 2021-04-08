---
title: WM_SETHOTKEY Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, um dem Fenster einen Hot-Schlüssel zuzuordnen. Wenn der Benutzer die Taste "heiß" drückt, aktiviert das System das Fenster.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Tastatur-und Maus Eingaben für WM_SETHOTKEY Nachricht
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "103761514"
---
# <a name="wm_sethotkey-message"></a>WM- \_ Nachricht "abkthotkey"

Wird an ein Fenster gesendet, um dem Fenster einen Hot-Schlüssel zuzuordnen. Wenn der Benutzer die Taste "heiß" drückt, aktiviert das System das Fenster.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt den Code des virtuellen Schlüssels an, der dem Fenster zugeordnet werden soll.

Bei dem höchst wertigen Wort kann es sich um einen oder mehrere der folgenden Werte aus "kommctrl. h" handeln.

Wenn Sie *wParam* auf **null** festlegen, wird der einem Fenster zugeordnete "Hot Key" entfernt.



| Wert                                                                                                                                                                                                                         | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**Hotkeyf \_ ALT**</dt> <dt>0x04</dt> </dl>             | ALT-TASTE<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**Hotkeyf \_ Steuer**</dt> Element <dt>0x02</dt> </dl> | STRG-Taste<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**Hotkeyf \_ EXT**</dt> <dt>0x08</dt> </dl>             | Erweiterter Schlüssel<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**Hotkeyf \_ UMSCHALT**</dt> <dt>0x01</dt> </dl>       | Umschalttaste<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Werte.



| Rückgabewert                                                                  | BESCHREIBUNG                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | Die Funktion ist nicht erfolgreich. die Hot-Taste ist ungültig.<br/>                        |
| <dl> <dt>0</dt> </dl>  | Die Funktion ist nicht erfolgreich. Das Fenster ist ungültig.<br/>                         |
| <dl> <dt>1</dt> </dl>  | Die Funktion ist erfolgreich, und kein anderes Fenster hat dieselbe heiße Taste.<br/>        |
| <dl> <dt>2</dt> </dl>  | Die Funktion ist erfolgreich, aber ein anderes Fenster hat bereits dieselbe heiße Taste.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein "Hot"-Schlüssel kann keinem untergeordneten Fenster zugeordnet werden.

**VK \_ Escape**, **VK \_ Space** und die **\_ Registerkarte VK** sind ungültige heiße Schlüssel.

Wenn der Benutzer die Taste "heiß" drückt, generiert das System eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht mit *wParam* -Wert **SC \_ Hotkey** und *LPARAM* gleich dem Handle des Fensters. Wenn diese Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)weitergegeben wird, führt das System das letzte aktive Popup Fenster (sofern vorhanden) oder das Fenster selbst (wenn es kein Popup Fenster gibt) im Vordergrund aus.

Ein Fenster kann nur über eine heiße Taste verfügen. Wenn dem Fenster bereits ein Abkürzungs Schlüssel zugeordnet ist, ersetzt die neue heiße Taste die alte. Wenn mehr als ein Fenster die gleiche Abkürzungs Taste hat, ist das Fenster, das von der Hot-Taste aktiviert wird, zufällig.

Diese Hotkeys sind nicht mit den von [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)festgelegten Hotkeys verknüpft.

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM- \_ GetHotKey**](wm-gethotkey.md)
</dt> <dt>

[**WM ( \_ syscommand)**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

