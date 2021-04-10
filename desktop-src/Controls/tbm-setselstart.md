---
title: TBM_SETSELSTART Meldung (kommstrg. h)
description: Legt die logische Startposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den \_ enableselrange-Stil von TB verfügt.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Windows-Steuerelemente für TBM_SETSELSTART Meldung
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
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040087"
---
# <a name="tbm_setselstart-message"></a>TBM- \_ setselstart-Meldung

Legt die logische Startposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Auswahlbereich festgelegt wurde. Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Auswahlbereich fest, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Anfangsposition des Auswahl Bereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TBM- \_ getselend**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ getselstart**](tbm-getselstart.md)
</dt> <dt>

[**TBM- \_ Sekunden**](tbm-setsel.md)
</dt> <dt>

[**TBM- \_ setselend**](tbm-setselend.md)
</dt> </dl>

 

 





