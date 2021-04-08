---
title: TBM_SETSELEND Meldung (kommstrg. h)
description: Legt die logische Endposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den \_ enableselrange-Stil von TB verfügt.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- Windows-Steuerelemente für TBM_SETSELEND Meldung
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
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102862"
---
# <a name="tbm_setselend-message"></a>TBM- \_ setselend-Nachricht

Legt die logische Endposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Auswahlbereich festgelegt wurde. Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Auswahlbereich fest, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Endende logische Position des Auswahl Bereichs.

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

[**TBM- \_ setselstart**](tbm-setselstart.md)
</dt> </dl>

 

 





