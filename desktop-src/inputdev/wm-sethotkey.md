---
title: WM_SETHOTKEY (Winuser.h)
description: Wird an ein Fenster gesendet, um dem Fenster einen heißen Schlüssel zu zuordnen. Wenn der Benutzer die hot-Taste drückt, aktiviert das System das Fenster.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY der Tastatur- und Mauseingabe
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
ms.openlocfilehash: 4b6c9d4bdb4a59181fe3a413cca6861bc3663367cca9e7b34e0647de88978b0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482517"
---
# <a name="wm_sethotkey-message"></a>WM \_ SETHOTKEY-Meldung

Wird an ein Fenster gesendet, um dem Fenster einen heißen Schlüssel zu zuordnen. Wenn der Benutzer die hot-Taste drückt, aktiviert das System das Fenster.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt den virtuellen Schlüsselcode an, der dem Fenster zugeordnet werden soll.

Das obere Wort kann einer oder mehrere der folgenden Werte aus CommCtrl.h sein.

Wenn *wParam auf* **NULL festgelegt wird,** wird der einem Fenster zugeordnete hot-Schlüssel entfernt.



| Wert                                                                                                                                                                                                                         | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ ALT-0x04**</dt> <dt></dt> </dl>             | ALT-TASTE<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_ CONTROL**</dt> <dt>0x02</dt> </dl> | STRG-TASTE<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_ EXT**</dt> <dt>0x08</dt> </dl>             | Erweiterter Schlüssel<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_ UMSCHALT 0X01**</dt> <dt></dt> </dl>       | Umschalttaste<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden.



| Rückgabewert                                                                  | BESCHREIBUNG                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | Die Funktion ist nicht erfolgreich. Der hot-Schlüssel ist ungültig.<br/>                        |
| <dl> <dt>0</dt> </dl>  | Die Funktion ist nicht erfolgreich. das Fenster ist ungültig.<br/>                         |
| <dl> <dt>1</dt> </dl>  | Die Funktion ist erfolgreich, und kein anderes Fenster verfügt über den gleichen heißen Schlüssel.<br/>        |
| <dl> <dt>2</dt> </dl>  | Die Funktion ist erfolgreich, aber ein anderes Fenster verfügt bereits über den gleichen heißen Schlüssel.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein hot-Schlüssel kann nicht einem untergeordneten Fenster zugeordnet werden.

**VK \_ ESCAPE,** **VK \_ SPACE** und **VK \_ TAB** sind ungültige Hot Keys.

Wenn der Benutzer die hot-Taste drückt, generiert das System eine [**WM \_ SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) mit *wParam* gleich **SC \_ HOTKEY** und *lParam* gleich dem Handle des Fensters. Wenn diese Meldung an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben wird, bringt das System das letzte aktive Popupfenster des Fensters (sofern vorhanden) oder das Fenster selbst (wenn kein Popupfenster vorhanden ist) in den Vordergrund.

Ein Fenster kann nur einen hot-Schlüssel haben. Wenn dem Fenster bereits ein hot-Schlüssel zugeordnet ist, ersetzt der neue hot-Schlüssel den alten. Wenn mehr als ein Fenster über den gleichen heißen Schlüssel verfügt, ist das Fenster, das durch den heißen Schlüssel aktiviert wird, zufällig.

Diese heißen Schlüssel stehen nicht mit den hot-Schlüsseln in Zusammenhang, die von [**RegisterHotKey festgelegt werden.**](/windows/win32/api/winuser/nf-winuser-registerhotkey)

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

