---
title: TBM_GETSELSTART-Nachricht (Commctrl.h)
description: Ruft die Anfangsposition des aktuellen Auswahlbereichs in einer Trackleiste ab.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- TBM_GETSELSTART Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a654bfcf8756bee5b39ec9fc97b82ffe84e8e48ba39f4ca2f9fab732d0d1962e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046420"
---
# <a name="tbm_getselstart-message"></a>TBM \_ GETSELSTART-Nachricht

Ruft die Anfangsposition des aktuellen Auswahlbereichs in einer Trackleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Anfangsposition des aktuellen Auswahlbereichs angibt.

## <a name="remarks"></a>Hinweise

Eine Trackleiste kann nur einen Auswahlbereich aufweisen, wenn Sie beim Erstellen den [**\_ TBS-STIL "ENABLESELRANGE"**](trackbar-control-styles.md) angegeben haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





