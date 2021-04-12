---
title: RB_MOVEBAND Meldung (kommstrg. h)
description: Verschiebt ein Band von einem Index zu einem anderen.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Windows-Steuerelemente für RB_MOVEBAND Meldung
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475342"
---
# <a name="rb_moveband-message"></a>RB- \_ Message-Nachricht

Verschiebt ein Band von einem Index zu einem anderen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des zu bewegenden Bands.

</dd> <dt>

*lParam* 
</dt> <dd>

NULL basierter Index der neuen Bandposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ändert höchstwahrscheinlich den Index anderer Bänder im Grund leisten-Steuerelement. Wenn ein Band von Index 6 in Index 0 verschoben wird, wird der Index aller Bänder dazwischen um 1 erhöht.

*LPARAM* darf nie größer als die Anzahl der Bänder minus 1 sein. Die Anzahl der Bänder kann mit der [**RB \_ GetBandCount**](rb-getbandcount.md) -Nachricht abgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





