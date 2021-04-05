---
title: PBM_GETBKCOLOR Meldung (kommstrg. h)
description: Ruft die Hintergrundfarbe der Statusanzeige ab.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Windows-Steuerelemente für PBM_GETBKCOLOR Meldung
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
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859074"
---
# <a name="pbm_getbkcolor-message"></a>PBM \_ GetBkColor-Nachricht

Ruft die Hintergrundfarbe der Statusanzeige ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Hintergrundfarbe der Statusanzeige zurück.

## <a name="remarks"></a>Bemerkungen

Dies ist die Farbe, die von der [**PBM- \_ SetBkColor**](pbm-setbkcolor.md) -Nachricht festgelegt wird. Der Standardwert ist CLR \_ Default, der in "kommctrl. h" definiert ist.

Diese Funktion wirkt sich nur auf den klassischen Modus aus, nicht auf einen visuellen Stil.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





