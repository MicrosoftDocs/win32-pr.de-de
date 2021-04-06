---
title: HDM_SETBITMAPMARGIN Meldung (kommstrg. h)
description: Legt die Breite des in Pixel angegebenen Rands einer Bitmap in einem vorhandenen Header Steuerelement fest. Sie können diese Nachricht explizit senden oder das-Header \_ setbitmapmargin-Makro verwenden.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Windows-Steuerelemente für HDM_SETBITMAPMARGIN Meldung
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859128"
---
# <a name="hdm_setbitmapmargin-message"></a>HDM- \_ setbitmapmargin-Meldung

Legt die Breite des in Pixel angegebenen Rands einer Bitmap in einem vorhandenen Header Steuerelement fest. Sie können diese Nachricht explizit senden oder das- [**Header \_ setbitmapmargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die in Pixel angegebene Breite des Randes, das eine Bitmap in einem vorhandenen Header Steuerelement umgibt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Breite des bitmaprandes in Pixel zurück. Wenn der bitmaprand zuvor nicht angegeben wurde, wird der Standardwert 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ cxedge*) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HDM \_ getbitmapmargin**](hdm-getbitmapmargin.md)
</dt> </dl>

 

