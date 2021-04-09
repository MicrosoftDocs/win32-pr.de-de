---
title: PGM_GETBUTTONSIZE Meldung (kommstrg. h)
description: Ruft die aktuelle Schaltflächen Größe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager- \_ getbuttonsize-Makro verwenden.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Windows-Steuerelemente für PGM_GETBUTTONSIZE Meldung
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040797"
---
# <a name="pgm_getbuttonsize-message"></a>PGM- \_ getbuttonsize-Nachricht

Ruft die aktuelle Schaltflächen Größe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ getbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die aktuelle Schaltflächen Größe in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PGM \_ setbuttonsize**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





