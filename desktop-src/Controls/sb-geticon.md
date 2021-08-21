---
title: SB_GETICON (Commctrl.h)
description: Ruft das Symbol für ein Teil in einer Statusleiste ab.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3df97598c1b002a794badb54f727632d58cc915f216947c019e452f5632a09fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168766"
---
# <a name="sb_geticon-message"></a>SB \_ GETICON-Nachricht

Ruft das Symbol für ein Teil in einer Statusleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Teils, der das abzurufende Symbol enthält. Wenn dieser Parameter -1 ist, wird davon ausgegangen, dass es sich bei der Statusleiste um eine Statusleiste im [einfachen](status-bars.md) Modus handelt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an das Symbol zurück, wenn erfolgreich, **andernfalls NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





