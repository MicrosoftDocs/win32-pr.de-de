---
title: EM_GETCTFMODEBIAS (Richedit.h)
description: Ruft die Textdienstframework modus bias-Werte für ein Microsoft Rich Edit-Steuerelement ab.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d6e030e3080ec9bf3d801583b9ade182483ba8560b3eccb2fb9813be7d39cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019748"
---
# <a name="em_getctfmodebias-message"></a>EM \_ GETCTFMODEBIAS-Nachricht

Ruft die Textdienstframework modus bias-Werte für ein Microsoft Rich Edit-Steuerelement ab.

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

Der aktuelle Textdienstframework-Modus-Biaswert.

## <a name="remarks"></a>Hinweise

Rufen Sie EM [**\_ GETIMEMODEBIAS**](em-getimemodebias.md)auf, um den IME-Modus zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





