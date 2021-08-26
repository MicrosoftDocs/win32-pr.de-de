---
title: EM_CALLAUTOCORRECTPROC Nachricht (Richedit.h)
description: Ruft die autocorrect-Rückruffunktion auf, die von der EM \_ SETAUTOCORRECTPROC-Nachricht gespeichert wird, vorausgesetzt, dass der Text vor der Einfügemarke ein Kandidat für die autocorrection ist.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad76ec66018b4e673913c433ce16a1294944f69c9d33a5dbaedb85ba21f985a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916080"
---
# <a name="em_callautocorrectproc-message"></a>EM \_ CALLAUTOCORRECTPROC-Nachricht

Ruft die autocorrect-Rückruffunktion auf, die von der [**EM \_ SETAUTOCORRECTPROC-Nachricht**](em-setautocorrectproc.md) gespeichert wird, vorausgesetzt, dass der Text vor der Einfügemarke ein Kandidat für die autocorrection ist.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeichen vom Typ **WCHAR**. Wenn es sich bei diesem Zeichen um eine Registerkarte (U+0009) handelt und das Zeichen vor der Einfügemarke keine Registerkarte ist, wird das Zeichen vor der Einfügemarke nicht als Zeichenfolgentrennzeichen, sondern als Teil der Kandidatenzeichenfolge autocorrect behandelt. Andernfalls hat *wParam* keine Auswirkungen.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist 0 (null), wenn die Nachricht erfolgreich ist, oder ungleich 0 (null), wenn ein Fehler auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





