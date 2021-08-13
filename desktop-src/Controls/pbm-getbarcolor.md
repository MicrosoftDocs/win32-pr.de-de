---
title: PBM_GETBARCOLOR (Commctrl.h)
description: Ruft die Farbe der Statusleiste ab.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312440"
---
# <a name="pbm_getbarcolor-message"></a>PBM \_ GETBARCOLOR-Nachricht

Ruft die Farbe der Statusleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Farbe der Statusleiste zurück.

## <a name="remarks"></a>Hinweise

Dies ist die Farbe, die von der [**PBM \_ SETBARCOLOR-Meldung festgelegt**](pbm-setbarcolor.md) wird. Der Standardwert ist CLR \_ DEFAULT, der in commctrl.h definiert ist.

Diese Funktion wirkt sich nur auf den klassischen Modus aus, nicht auf visuelle Stile.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





