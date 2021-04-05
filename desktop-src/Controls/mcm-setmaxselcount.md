---
title: MCM_SETMAXSELCOUNT Meldung (kommstrg. h)
description: Legt die maximale Anzahl von Tagen fest, die in einem Monatskalender-Steuerelement ausgewählt werden können. Sie können diese Nachricht explizit oder mit dem monthcal \_ setmaxselcount-Makro senden.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- Windows-Steuerelemente für MCM_SETMAXSELCOUNT Meldung
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859243"
---
# <a name="mcm_setmaxselcount-message"></a>MCM \_ setmaxselcount-Nachricht

Legt die maximale Anzahl von Tagen fest, die in einem Monatskalender-Steuerelement ausgewählt werden können. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ setmaxselcount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert vom Typ **int** , der so festgelegt wird, dass die maximale Anzahl von Tagen, die ausgewählt werden können, dargestellt wird.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. Diese Nachricht schlägt fehl, wenn Sie auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





