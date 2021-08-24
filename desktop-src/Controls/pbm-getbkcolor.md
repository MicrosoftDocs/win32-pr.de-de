---
title: PBM_GETBKCOLOR Meldung (Commctrl.h)
description: Ruft die Hintergrundfarbe der Statusanzeige ab.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919520"
---
# <a name="pbm_getbkcolor-message"></a>PBM \_ GETBKCOLOR-Nachricht

Ruft die Hintergrundfarbe der Statusanzeige ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Hintergrundfarbe der Statusanzeige zurück.

## <a name="remarks"></a>Hinweise

Dies ist die Farbe, die von der [**PBM \_ SETBKCOLOR-Nachricht**](pbm-setbkcolor.md) festgelegt wird. Der Standardwert ist CLR \_ DEFAULT, der in commctrl.h definiert ist.

Diese Funktion wirkt sich nur auf den klassischen Modus und nicht auf visuelle Stile aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





