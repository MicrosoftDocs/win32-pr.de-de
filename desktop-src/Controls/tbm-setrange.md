---
title: TBM_SETRANGE Meldung (kommstrg. h)
description: Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer TrackBar fest.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Windows-Steuerelemente für TBM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040359"
---
# <a name="tbm_setrange-message"></a>TBM- \_ Nachricht

Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer TrackBar fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, wird die TrackBar nach dem Festlegen des Bereichs neu gezeichnet. Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Bereich fest, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die minimale Position für den Schieberegler an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die maximale Position an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn sich die aktuelle Position des Schiebereglers außerhalb des neuen Bereichs befindet, legt die **TBM- \_ SetRange** -Nachricht die Schiebereglerposition auf den neuen maximalen oder minimalen Wert fest.

Da diese Nachricht 2 16-Bit-ganz Zahl Werte ohne Vorzeichen annimmt, liegt der maximale Bereich, den diese Meldung angeben kann, zwischen 0 und 65.535. Um größere Bereichs Werte anzugeben, verwenden Sie die TBM-Nachrichten " [**TBM \_**](tbm-setrangemin.md) " und " [**TBM \_**](tbm-setrangemax.md) ".

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

[**TBM-Objekt- \_ Max**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ -Anpassung**](tbm-setrangemin.md)
</dt> </dl>

 

