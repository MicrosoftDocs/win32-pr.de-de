---
title: TBM_SETRANGEMIN Meldung (kommstrg. h)
description: Legt die minimale logische Position für den Schieberegler in einer TrackBar fest.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Windows-Steuerelemente für TBM_SETRANGEMIN Meldung
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949411"
---
# <a name="tbm_setrangemin-message"></a>TBM- \_ Nachricht

Legt die minimale logische Position für den Schieberegler in einer TrackBar fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Bereich festgelegt wurde. Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Bereich fest, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Minimale Position für den Schieberegler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn die aktuelle Position des Schiebereglers kleiner ist als der neue Minimalwert, legt die **TBM- \_ SetRangeMin** -Meldung die Schiebereglerposition auf den neuen Minimalwert fest.

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

[**TBM-über \_ Tragung**](tbm-setrange.md)
</dt> <dt>

[**TBM-Objekt- \_ Max**](tbm-setrangemax.md)
</dt> </dl>

 

 





