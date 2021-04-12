---
title: EM_SETAUTOCORRECTPROC Meldung (RichEdit. h)
description: Definiert die aktuelle AutoKorrektur-Rückruf Prozedur.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Windows-Steuerelemente für EM_SETAUTOCORRECTPROC Meldung
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478591"
---
# <a name="em_setautocorrectproc-message"></a>EM- \_ Nachricht

Definiert die aktuelle AutoKorrektur-Rückruf Prozedur.


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die [*autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) -Rückruffunktion.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert 0 (null). Wenn der Vorgang fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[*Autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ callautocorrectproc**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ getautocorrectproc**](em-getautocorrectproc.md)
</dt> </dl>

 

 





