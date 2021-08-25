---
title: SB_GETBORDERS-Nachricht (Commctrl.h)
description: Ruft die aktuelle Breite des horizontalen und vertikalen Rahmens eines Statusfensters ab.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafa7a8c27b5c274a981e43edc5c55ec0cade67cac08a1d09a898916d792795c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169053"
---
# <a name="sb_getborders-message"></a>SB \_ GETBORDERS-Nachricht

Ruft die aktuelle Breite des horizontalen und vertikalen Rahmens eines Statusfensters ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein ganzzahliges Array, das drei Elemente enthält. Das erste Element empfängt die Breite des horizontalen Rahmens, das zweite erhält die Breite des vertikalen Rahmens, und das dritte erhält die Breite des Rahmens zwischen Rechtecke.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Die Rahmen bestimmen den Abstand zwischen dem äußeren Rand des Fensters und den Rechtecke im Fenster, die Text enthalten. Die Rahmen bestimmen auch den Abstand zwischen Rechtecke.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





