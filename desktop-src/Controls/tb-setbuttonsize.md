---
title: TB_SETBUTTONSIZE-Nachricht (Commctrl.h)
description: Legt die Größe von Schaltflächen auf einer Symbolleiste fest.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b0b957ad6328515da7aee2f978870662801aa6aba81133e9e4bc22ee7d9c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167733"
---
# <a name="tb_setbuttonsize-message"></a>TB \_ SETBUTTONSIZE-Nachricht

Legt die Größe von Schaltflächen auf einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Breite der Schaltflächen in Pixel an. [**HiWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Höhe der Schaltflächen in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

**TB \_ SETBUTTONSIZE** sollte im Allgemeinen nach dem Hinzufügen von Schaltflächen aufgerufen werden.

Verwenden Sie [**TB \_ SETBUTTONWIDTH,**](tb-setbuttonwidth.md) um die maximal und minimal zulässigen Breiten für Schaltflächen festzulegen, bevor sie hinzugefügt werden. Verwenden Sie **TB \_ SETBUTTONSIZE,** um die tatsächliche Größe von Schaltflächen festzulegen.

## <a name="examples"></a>Beispiele

Im folgenden Beispielcode wird die Breite der Schaltflächen auf 80 Pixel und die Höhe auf 30 Pixel festgelegt.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

