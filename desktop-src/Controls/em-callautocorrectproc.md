---
title: EM_CALLAUTOCORRECTPROC Meldung (RichEdit. h)
description: Ruft die AutoKorrektur-Rückruffunktion auf, die von der EM-Nachricht "* \_ taudecorrectproc" gespeichert wird, vorausgesetzt, dass der Text vor der Einfügemarke ein Kandidat für die automatische Korrektur ist.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Windows-Steuerelemente für EM_CALLAUTOCORRECTPROC Meldung
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
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477625"
---
# <a name="em_callautocorrectproc-message"></a>EM \_ callautocorrectproc-Meldung

Ruft die AutoKorrektur-Rückruffunktion auf, die von der EM-Nachricht "* [**\_ taudecorrectproc**](em-setautocorrectproc.md) " gespeichert wird, vorausgesetzt, dass der Text vor der Einfügemarke ein Kandidat für die automatische Korrektur ist.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeichen vom Typ **WCHAR**. Wenn dieses Zeichen ein Tabulator Zeichen (U + 0009) ist und das Zeichen, das der Einfügemarke vorangestellt ist, ein Tabulator ist, wird das vor der Einfügemarke vorangehende Zeichen als Teil der AutoKorrektur Candidate-Zeichenfolge und nicht als Zeichen folgen Trennzeichen behandelt. Andernfalls hat *wParam* keine Auswirkung.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist 0 (null), wenn die Nachricht erfolgreich ist, oder ungleich NULL, wenn ein Fehler auftritt.

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

[**EM \_ getautocorrectproc**](em-getautocorrectproc.md)
</dt> <dt>

[**EM- \_ tautkorrigitproc**](em-setautocorrectproc.md)
</dt> </dl>

 

 





