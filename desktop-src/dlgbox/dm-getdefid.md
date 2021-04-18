---
title: DM_GETDEFID Meldung (Winuser. h)
description: Ruft den Bezeichner des Standard Steuer Elements für die pushschaltfläche für ein Dialogfeld ab.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Dialog Felder DM_GETDEFID Meldung
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518881"
---
# <a name="dm_getdefid-message"></a>DM \_ getdefid-Meldung

Ruft den Bezeichner des Standard Steuer Elements für die pushschaltfläche für ein Dialogfeld ab.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
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

Wenn eine Standard-Push-Schaltfläche vorhanden ist, enthält das hochwertige Wort des Rückgabewerts den Wert **DC \_ hasdefid** , und das nieder wertige Wort enthält den Steuerelement Bezeichner. Andernfalls ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Funktion [**defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) verarbeitet diese Nachricht.

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

[**Defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ -setdefid**](dm-setdefid.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> </dl>

 

 





