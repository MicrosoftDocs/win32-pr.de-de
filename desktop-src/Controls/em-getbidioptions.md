---
title: EM_GETBIDIOPTIONS (Richedit.h)
description: Gibt den aktuellen Zustand der bidirektionalen Optionen im Rich-Edit-Steuerelement an.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS von Windows Steuerelementen
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b377e0fd3a439737fea9efbc403d2ccc64d6cf78eab1c7e31feeffd6c4b0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019908"
---
# <a name="em_getbidioptions-message"></a>EM \_ GETBIDIOPTIONS-Nachricht

Gibt den aktuellen Zustand der bidirektionalen Optionen im Rich-Edit-Steuerelement an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**BIDIOPTIONS-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) die den aktuellen Zustand der bidirektionalen Optionen im Rich-Edit-Steuerelement empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung legt die Werte der **wMask-** und **wEffects-Member** auf den Wert des aktuellen Zustands der bidirektionalen Optionen im Rich Edit-Steuerelement fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ SETBIDIOPTIONS**](em-setbidioptions.md)
</dt> </dl>

 

 





