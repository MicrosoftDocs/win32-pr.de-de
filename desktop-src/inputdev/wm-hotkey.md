---
title: WM_HOTKEY Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine von der RegisterHotKey-Funktion registrierte heiße Taste drückt. Die Nachricht wird am Anfang der Nachrichten Warteschlange platziert, die dem Thread zugeordnet ist, der den Hot Key registriert hat.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- Tastatur-und Maus Eingaben für WM_HOTKEY Nachricht
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f09e81a964542a6a8166ae54a0df4d7127466c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391794"
---
# <a name="wm_hotkey-message"></a>WM- \_ Hotkey-Nachricht

Wird gesendet, wenn der Benutzer eine von der [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) -Funktion registrierte heiße Taste drückt. Die Nachricht wird am Anfang der Nachrichten Warteschlange platziert, die dem Thread zugeordnet ist, der den Hot Key registriert hat.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner des Hot-Schlüssels, der die Meldung generiert hat. Wenn die Meldung von einem System definierten Hot Key generiert wurde, ist dieser Parameter einer der folgenden Werte.



| Wert                                                                                                                                                                                                                             | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**Idhot \_ Snapdesktop**</dt> <dt>-2</dt> </dl> | Die Hot-Taste "Snap-in-Desktop" wurde gedrückt.<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**Idhot \_ Snapwindow**</dt> <dt>-1</dt> </dl>    | Die Hot-Taste des "Snap-Ins" wurde gedrückt.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Mit dem nieder wertigen Wort werden die Schlüssel angegeben, die in Kombination mit dem Schlüssel gedrückt werden sollen, der durch das hochwertige Wort zum Generieren der **WM- \_ Hotkey** -Nachricht angegeben wird. Bei diesem Wort kann es sich um einen oder mehrere der folgenden Werte handeln. Das höchst wertige Wort gibt den Code des virtuellen Schlüssels für den Hot Key an.



| Wert                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**Mod \_ ALT**</dt> <dt>0x0001</dt> </dl>             | Die Alt-Taste wurde gedrückt.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**Mod \_ Steuer**</dt> Element <dt>0x0002</dt> </dl> | Die STRG-Taste wurde gedrückt.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**Mod \_ UMSCHALT**</dt> <dt>0x0004</dt> </dl>       | Entweder wurde die UMSCHALTTASTE gedrückt.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**Mod \_ Win**</dt> <dt>0x0008</dt> </dl>             | Beide Windows-Schlüssel wurden angehalten. Diese Schlüssel werden mit dem Windows-Logo bezeichnet. Hotkeys, die den Windows-Schlüssel einschließen, sind für die Verwendung durch das Betriebssystem reserviert.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**WM \_ Hotkey** steht nicht in Zusammenhang mit den Abkürzungs Schlüsseln " [**\_ GetHotKey**](wm-gethotkey.md) " und " [**WM- \_ Schlüssel**](wm-sethotkey.md) ". Die **WM- \_ Hotkey** -Nachricht wird für generische Hotkeys gesendet, während die Nachrichten "WM-Host **\_ Schlüssel** " und " **WM \_ GetHotKey** " sich auf die Fenster Aktivierungs-Hotkeys beziehen.

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

[**WM- \_ Objekt Schlüssel**](wm-sethotkey.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

