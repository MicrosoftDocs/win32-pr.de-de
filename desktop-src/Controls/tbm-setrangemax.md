---
title: TBM_SETRANGEMAX (Commctrl.h)
description: Legt die maximale logische Position für den Schieberegler in einer Trackleiste fest.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- TBM_SETRANGEMAX meldungssteuerelemente Windows
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
ms.openlocfilehash: f26b4a588e67164b96db8256116466206d0274a5bc64caedbcb1ccf25135ce62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829593"
---
# <a name="tbm_setrangemax-message"></a>TBM \_ SETRANGEMAX-Nachricht

Legt die maximale logische Position für den Schieberegler in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu gezeichnet. Wenn dieser Parameter **TRUE ist,** wird die Trackleiste neu gezeichnet, nachdem der Bereich festgelegt wurde. Wenn dieser Parameter **FALSE ist,** legt die Meldung den Bereich fest, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>

Maximale Position für den Schieberegler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn die aktuelle Position des Schiebereglers größer als der neue Höchstwert ist, legt die **TBM \_ SETRANGEMAX-Meldung** die Position des Schiebereglers auf den neuen Höchstwert fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

 





