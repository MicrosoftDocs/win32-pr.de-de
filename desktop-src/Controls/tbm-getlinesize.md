---
title: TBM_GETLINESIZE Meldung (kommstrg. h)
description: Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- Windows-Steuerelemente für TBM_GETLINESIZE Meldung
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
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957244"
---
# <a name="tbm_getlinesize-message"></a>TBM \_ getlinesize-Meldung

Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Zeilengröße für die TrackBar angibt.

## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung für die Zeilengröße ist 1.

Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e/a \_ -und TB- \_ LineDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





