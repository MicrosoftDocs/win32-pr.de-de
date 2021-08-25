---
title: EM_SETCTFOPENSTATUS (Richedit.h)
description: Öffnet oder schließt die TASTATUR Textdienstframework (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ac27017abbadeb038f5b881aefe1aff394036931529c84c9c5a34a36e556c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048630"
---
# <a name="em_setctfopenstatus-message"></a>EM \_ SETCTFOPENSTATUS-Meldung

Öffnet oder schließt die TASTATUR Textdienstframework (TSF).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Um die TSF-Tastatur zu aktivieren, verwenden Sie **TRUE**. Verwenden Sie FALSE, um die TSF-Tastatur **zu deaktivieren.**

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dies erfolgreich ist, gibt diese Meldung **TRUE zurück.** Wenn dies nicht erfolgreich ist, gibt diese Meldung **FALSE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)
</dt> </dl>

 

 





