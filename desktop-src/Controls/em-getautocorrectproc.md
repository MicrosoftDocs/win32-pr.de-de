---
title: EM_GETAUTOCORRECTPROC Meldung (RichEdit. h)
description: Ruft einen Zeiger auf die Anwendungs definierte autocorrectproc-Funktion ab.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Windows-Steuerelemente für EM_GETAUTOCORRECTPROC Meldung
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477115"
---
# <a name="em_getautocorrectproc-message"></a>EM \_ getautocorrectproc-Nachricht

Ruft einen Zeiger auf die Anwendungs definierte [*autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) -Funktion ab.

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

Gibt einen Zeiger auf die Anwendungs definierte [*autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) -Funktion zurück.

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

[**EM- \_ tautkorrigitproc**](em-setautocorrectproc.md)
</dt> </dl>

 

 





