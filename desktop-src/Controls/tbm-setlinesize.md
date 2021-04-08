---
title: TBM_SETLINESIZE Meldung (kommstrg. h)
description: Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- Windows-Steuerelemente für TBM_SETLINESIZE Meldung
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949545"
---
# <a name="tbm_setlinesize-message"></a>TBM- \_ Nachricht "setlinesize"

Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Zeilengröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die vorherige Zeilengröße angibt.

## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung für die Zeilengröße ist 1.

Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e/a \_ -und TB- \_ LineDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TBM \_ getlinesize**](tbm-getlinesize.md)
</dt> </dl>

 

 





