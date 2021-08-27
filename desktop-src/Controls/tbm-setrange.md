---
title: TBM_SETRANGE (Commctrl.h)
description: Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer Trackleiste fest.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE meldungssteuerelemente Windows
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
ms.openlocfilehash: dfcd4bf71cfcbc36e098bc83568bdf519209ec82cc9889b6b5ec3934d349f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061140"
---
# <a name="tbm_setrange-message"></a>TBM \_ SETRANGE-Meldung

Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu gezeichnet. Wenn dieser Parameter **TRUE ist,** wird die Trackleiste neu gezeichnet, nachdem der Bereich festgelegt wurde. Wenn dieser Parameter **FALSE ist,** legt die Meldung den Bereich fest, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die Mindestposition für den Schieberegler an, und [**das HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die maximale Position an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn sich die aktuelle Position des Schiebereglers außerhalb des neuen Bereichs befindet, legt die **TBM \_ SETRANGE-Meldung** die Position des Schiebereglers auf den neuen höchst- oder minimalen Wert fest.

Da diese Nachricht zwei 16-Bit-Ganzzahlwerte ohne Vorzeichen angibt, liegt der maximale Bereich, den diese Nachricht angeben kann, zwischen 0 und 65.535. Verwenden Sie zum Angeben größerer Bereichswerte die [**\_ TBM-Meldungen SETRANGEMIN**](tbm-setrangemin.md) und [**TBM \_ SETRANGEMAX.**](tbm-setrangemax.md)

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

