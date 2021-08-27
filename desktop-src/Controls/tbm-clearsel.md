---
title: TBM_CLEARSEL (Commctrl.h)
description: Löschen des aktuellen Auswahlbereichs in einer Trackleiste.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- TBM_CLEARSEL meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 627f2c872b47bf76312856fd81d42bfe8f2739e53efb3c37492b203b150b8e8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046760"
---
# <a name="tbm_clearsel-message"></a>TBM \_ CLEARSEL-Meldung

Löschen des aktuellen Auswahlbereichs in einer Trackleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu gezeichnet. Wenn dieser Parameter **TRUE ist,** wird die Trackleiste neu gezeichnet, nachdem die Auswahl wieder ausgewählt wurde.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Trackleiste kann nur dann einen Auswahlbereich haben, wenn Sie beim Erstellen den [**TBS \_ ENABLESELRANGE-Stil**](trackbar-control-styles.md) angegeben haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





