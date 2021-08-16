---
title: TBM_GETLINESIZE (Commctrl.h)
description: Ruft die Anzahl der logischen Positionen ab, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben über die Pfeiltasten bewegt, z. B. die Tasten oder . Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der minimalen bis maximalen Schiebereglerpositionen der Trackleiste.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE message Windows Controls
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6db69efda8a6836f8c366092871cbb6b54261021a69c80e2bb14abcd88d967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046560"
---
# <a name="tbm_getlinesize-message"></a>TBM \_ GETLINESIZE-Nachricht

Ruft die Anzahl der logischen Positionen ab, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben über die Pfeiltasten bewegt, z. B. die Tasten oder . Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der minimalen bis maximalen Schiebereglerpositionen der Trackleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Zeilengröße für die Trackleiste angibt.

## <a name="remarks"></a>Hinweise

Die Standardeinstellung für die Zeilengröße ist 1.

Die Trackleiste sendet auch eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) mit den TB \_ LINEUP- und TB LINEDOWN-Benachrichtigungscodes an das übergeordnete Fenster, wenn der Benutzer die \_ Pfeiltasten drückt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





