---
title: TB_GETITEMRECT (Commctrl.h)
description: Ruft das umgebundene Rechteck einer Schaltfläche in einer Symbolleiste ab.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT von Windows Steuerelementen
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6dbfa4c7e305c4e2dfe53b45edaac1d6601631c920fa266c64292fd7e6d97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829705"
---
# <a name="tb_getitemrect-message"></a>TB \_ GETITEMRECT-Nachricht

Ruft das umgebundene Rechteck einer Schaltfläche in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index der Schaltfläche, für die Informationen abgerufen werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Clientkoordinaten des umgebundenen Rechtecks empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Meldung ruft das umgebundene Rechteck für Schaltflächen, deren Zustand auf den [**TBSTATE \_ HIDDEN-Wert**](toolbar-button-states.md) festgelegt ist, nicht ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

