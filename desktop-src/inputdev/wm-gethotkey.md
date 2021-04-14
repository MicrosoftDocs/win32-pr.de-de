---
title: WM_GETHOTKEY Meldung (Winuser. h)
description: Wird gesendet, um den einem Fenster zugeordneten Hot-Schlüssel zu bestimmen.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Tastatur-und Maus Eingaben für WM_GETHOTKEY Nachricht
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476158"
---
# <a name="wm_gethotkey-message"></a>WM- \_ GetHotKey-Nachricht

Wird gesendet, um den einem Fenster zugeordneten Hot-Schlüssel zu bestimmen.


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Code und die modifiziererer des virtuellen Schlüssels für die Hot-Taste, oder **null** , wenn dem Fenster keine heiße Taste zugeordnet ist. Der Code für den virtuellen Schlüssel befindet sich im unteren Byte des Rückgabewerts, und die Modifizierer sind im hohen Byte. Die modifiziererer können eine Kombination der folgenden Flags aus "kommctrl. h" sein.



| Rückgabecode/-wert                                                                                                                                         | BESCHREIBUNG             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**Hotkeyf \_ ALT**</dt> <dt>0x04</dt> </dl>     | ALT-TASTE<br/>      |
| <dl> <dt>**Hotkeyf \_ Steuer**</dt> Element <dt>0x02</dt> </dl> | STRG-Taste<br/>     |
| <dl> <dt>**Hotkeyf \_ EXT**</dt> <dt>0x08</dt> </dl>     | Erweiterter Schlüssel<br/> |
| <dl> <dt>**Hotkeyf \_ UMSCHALT**</dt> <dt>0x01</dt> </dl>   | Umschalttaste<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Diese Hotkeys sind nicht mit den von der [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) -Funktion festgelegten Hotkeys verknüpft.

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

[**WM- \_ Objekt Schlüssel**](wm-sethotkey.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

