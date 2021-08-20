---
title: TBM_SETSELEND (Commctrl.h)
description: Legt die logische Endposition des aktuellen Auswahlbereichs in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über den TBS \_ ENABLESELRANGE-Stil verfügt.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ee524bf6a519a7d0071e4149ed03191a9aec989e2deefe596cca1072dbd098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167065"
---
# <a name="tbm_setselend-message"></a>TBM \_ SETSELEND-Nachricht

Legt die logische Endposition des aktuellen Auswahlbereichs in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über den [**TBS \_ ENABLESELRANGE-Stil**](trackbar-control-styles.md) verfügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu gezeichnet. Wenn dieser Parameter **TRUE ist,** wird die Trackleiste in der Meldung neu gedrammt, nachdem der Auswahlbereich festgelegt wurde. Wenn dieser Parameter **FALSE ist,** legt die Meldung den Auswahlbereich fest, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>

Beenden der logischen Position des Auswahlbereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

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

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





