---
title: DM_GETDEFID (Winuser.h)
description: Ruft den Bezeichner des standarden Schaltflächen-Steuerelements für ein Dialogfeld ab.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID Meldungsdialogfelder
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
ms.openlocfilehash: 6898ed6484a66e1c0d5fa498b0352498c0a57fbe91a74f738e2c6438511aef21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785822"
---
# <a name="dm_getdefid-message"></a>DM \_ GETDEFID-Nachricht

Ruft den Bezeichner des standarden Schaltflächen-Steuerelements für ein Dialogfeld ab.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
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

Wenn eine Standardschaltfläche vorhanden ist, enthält das obere Wort des Rückgabewerts den Wert **DC \_ HASDEFID,** und das niedrige Wort enthält den Steuerelementbezeichner. Andernfalls ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Die [**DefDlgProc-Funktion**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) verarbeitet diese Nachricht.

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ SETDEFID**](dm-setdefid.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> </dl>

 

 





