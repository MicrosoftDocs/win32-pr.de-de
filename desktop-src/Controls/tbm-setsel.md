---
title: TBM_SETSEL (Commctrl.h)
description: Legt die Anfangs- und Endpositionen für den verfügbaren Auswahlbereich in einer Trackleiste fest.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d055b317cc6db5e17edbe57bc57e6dbfe287274788718e8e2a920e1f25d9316b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829328"
---
# <a name="tbm_setsel-message"></a>TBM \_ SETSEL-Nachricht

Legt die Anfangs- und Endpositionen für den verfügbaren Auswahlbereich in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu gezeichnet. Wenn dieser Parameter **TRUE ist,** wird die Trackleiste in der Meldung neu gedrammt, nachdem der Auswahlbereich festgelegt wurde. Wenn dieser Parameter **FALSE ist,** legt die Meldung den Auswahlbereich fest, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die logische Anfangsposition für den Auswahlbereich an, und [**das HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die logische Endposition an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Meldung wird ignoriert, wenn die Trackleiste nicht über den [**TBS \_ ENABLESELRANGE-Stil**](trackbar-control-styles.md) verfügt.

**TBM \_ Mit SETSEL** können Sie den Zeiger auf einen Teil des Bereichs beschränken, der für die Statusleiste verfügbar ist.

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

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

