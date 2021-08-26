---
title: BCM_GETTEXTMARGIN (Commctrl.h)
description: Ruft die Ränder ab, die zum Zeichnen von Text in einem Schaltflächen-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das Button \_ GetTextMargin-Makro verwenden.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN der Windows Steuerelemente
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea871d0054558e1522011d4fdb00fdd3c82a0dd1562fe3420d3295bbab89a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064410"
---
# <a name="bcm_gettextmargin-message"></a>BCM \_ GETTEXTMARGIN-Nachricht

Ruft die Ränder ab, die zum Zeichnen von Text in einem Schaltflächen-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das [**Button \_ GetTextMargin-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Ränder enthält, die zum Zeichnen von Text verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Meldung erfolgreich ist, wird **TRUE zurückgegeben.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

