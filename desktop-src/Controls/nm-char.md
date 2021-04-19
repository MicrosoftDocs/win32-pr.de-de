---
title: NM_CHAR Benachrichtigungs Code (kommctrl. h)
description: Der nm \_ char-Benachrichtigungs Code wird von einem-Steuerelement gesendet, wenn eine Zeichen Taste verarbeitet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- Windows-Steuerelemente für NM_CHAR Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346773"
---
# <a name="nm_char-notification-code"></a>NM \_ char-Benachrichtigungs Code

Der nm \_ char-Benachrichtigungs Code wird von einem-Steuerelement gesendet, wenn eine Zeichen Taste verarbeitet wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmchar**](/windows/win32/api/commctrl/ns-commctrl-nmchar) -Struktur, die zusätzliche Informationen über das Zeichen enthält, das den Benachrichtigungs Code verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird von den meisten Steuerelementen ignoriert. Weitere Informationen finden Sie in der Dokumentation für die einzelnen Steuerelemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NM \_ char (Symbolleiste)](nm-char-toolbar.md)
</dt> </dl>

 

 





