---
title: TBM_SETRANGEMAX Meldung (kommstrg. h)
description: Legt die maximale logische Position für den Schieberegler in einer TrackBar fest.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Windows-Steuerelemente für TBM_SETRANGEMAX Meldung
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475135"
---
# <a name="tbm_setrangemax-message"></a>TBM- \_ Nachricht

Legt die maximale logische Position für den Schieberegler in einer TrackBar fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, wird die TrackBar nach dem Festlegen des Bereichs neu gezeichnet. Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Bereich fest, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Maximale Position für den Schieberegler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn die aktuelle Schieberegler-Position größer als die neue Höchstzahl ist, legt die **TBM \_ SetRangeMax** -Meldung die Schieberegler-Position auf den neuen maximalen Wert fest.

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

[**TBM \_ -Anpassung**](tbm-setrangemin.md)
</dt> </dl>

 

 





