---
title: TBM_SETSELSTART Meldung (Commctrl.h)
description: Legt die logische Anfangsposition des aktuellen Auswahlbereichs in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über das \_ TBS-FORMAT ENABLESELRANGE verfügt.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8cfdc938da5c7f5904e79f55177fe6f8eccba10f37dfdadb613c581cc809fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829314"
---
# <a name="tbm_setselstart-message"></a>TBM \_ SETSELSTART-Nachricht

Legt die logische Anfangsposition des aktuellen Auswahlbereichs in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über das [**\_ TBS-FORMAT ENABLESELRANGE**](trackbar-control-styles.md) verfügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neu gezeichnetes Flag. Wenn dieser Parameter **TRUE** ist, zeichnet die Nachricht die Trackleiste neu, nachdem der Auswahlbereich festgelegt wurde. Wenn dieser Parameter **FALSE** ist, legt die Nachricht den Auswahlbereich fest, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>

Anfangsposition des Auswahlbereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

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

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> </dl>

 

 





