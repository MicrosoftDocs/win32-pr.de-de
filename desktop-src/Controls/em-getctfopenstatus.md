---
title: EM_GETCTFOPENSTATUS (Richedit.h)
description: Bestimmt, ob die Textdienstframework (TSF) geöffnet oder geschlossen ist.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef55fe0944ad3632f8bfec11894c5613efde02dc1ec16f8c0d31105f6b19ea8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019738"
---
# <a name="em_getctfopenstatus-message"></a>EM \_ GETCTFOPENSTATUS-Nachricht

Bestimmt, ob die Textdienstframework (TSF) geöffnet oder geschlossen ist.

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

Wenn die TSF-Tastatur geöffnet ist, ist der Rückgabewert **TRUE.** Andernfalls ist dies **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETCTFOPENSTATUS**](em-setctfopenstatus.md)
</dt> </dl>

 

 





