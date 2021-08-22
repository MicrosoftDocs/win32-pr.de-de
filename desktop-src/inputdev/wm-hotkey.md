---
title: WM_HOTKEY (Winuser.h)
description: Wird veröffentlicht, wenn der Benutzer einen hot-Schlüssel drückt, der von der RegisterHotKey-Funktion registriert wurde. Die Nachricht wird am Anfang der Nachrichtenwarteschlange platziert, die dem Thread zugeordnet ist, der den heißen Schlüssel registriert hat.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- WM_HOTKEY der Tastatur- und Mauseingabe
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
ms.openlocfilehash: 51dbd37b61fea12e559323a73cbf6b4a5cb54704a74663f865d9aa89636d3c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557140"
---
# <a name="wm_hotkey-message"></a>WM \_ HOTKEY-Meldung

Wird veröffentlicht, wenn der Benutzer einen hot-Schlüssel drückt, der von der [**RegisterHotKey-Funktion registriert**](/windows/win32/api/winuser/nf-winuser-registerhotkey) wurde. Die Nachricht wird am Anfang der Nachrichtenwarteschlange platziert, die dem Thread zugeordnet ist, der den heißen Schlüssel registriert hat.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner des heißen Schlüssels, der die Nachricht generiert hat. Wenn die Nachricht von einem systemdefinierten heißen Schlüssel generiert wurde, ist dieser Parameter einer der folgenden Werte.



| Wert                                                                                                                                                                                                                             | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | Die heiße Taste "Desktop ausrichten" wurde gedrückt.<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | Die hot-Taste "Snap window" (Fenster ausrichten) wurde gedrückt.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt die Tasten an, die in Kombination mit dem schlüssel gedrückt werden sollen, der durch das hochgeordnete Wort angegeben wird, um die **WM \_ HOTKEY-Nachricht zu** generieren. Dieses Wort kann einer oder mehrere der folgenden Werte sein. Das hochgeordnete Wort gibt den virtuellen Schlüsselcode des heißen Schlüssels an.



| Wert                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**MOD \_ ALT-0x0001**</dt> <dt></dt> </dl>             | Beide ALT-Taste wurde gedrückt gehalten.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**MOD \_ CONTROL**</dt> <dt>0x0002</dt> </dl> | Beide STRG-Tasten wurden gedrückt gehalten.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**MOD \_ UMSCHALT 0X0004**</dt> <dt></dt> </dl>       | Beide UMSCHALTTASTEn wurden zurück gehalten.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**MOD \_ WIN-0x0008**</dt> <dt></dt> </dl>             | Beide WINDOWS-Schlüssel wurden zurück gehalten. Diese Schlüssel sind mit dem Windows gekennzeichnet. Hotkeys, die Windows Schlüssel beinhalten, sind für die Verwendung durch das Betriebssystem reserviert.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

**WM \_ HOTKEY** steht in keinem Zusammenhang mit den HOT-Schlüsseln [**WM \_ GETHOTKEY**](wm-gethotkey.md) und [**WM \_ SETHOTKEY.**](wm-sethotkey.md) Die **WM \_ HOTKEY-Nachricht** wird für generische hot-Schlüssel gesendet, während sich die **WM \_ SETHOTKEY-** und **WM \_ GETHOTKEY-Meldungen** auf hot-Schlüssel für die Fensteraktivierung beziehen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

