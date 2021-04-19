---
title: PGM_GETBORDER Meldung (kommstrg. h)
description: Ruft die aktuelle Rahmengröße für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager- \_ GetBorder-Makro verwenden.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Windows-Steuerelemente für PGM_GETBORDER Meldung
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339996"
---
# <a name="pgm_getborder-message"></a>PGM \_ GetBorder-Nachricht

Ruft die aktuelle Rahmengröße für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die aktuelle Rahmengröße in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PGM- \_ setborder**](pgm-setborder.md)
</dt> </dl>

 

 





