---
title: HDM_SETBITMAPMARGIN (Commctrl.h)
description: Legt die Breite des in Pixel angegebenen Rands einer Bitmap in einem vorhandenen Headersteuersatz fest. Sie können diese Nachricht explizit senden oder das \_ Header-Makro SetBitmapMargin verwenden.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN meldungssteuerelemente Windows
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
ms.openlocfilehash: aa2e7c24ea52edc0001cea9f4d7184957c2cfbf50f15769df964351df91e5813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435950"
---
# <a name="hdm_setbitmapmargin-message"></a>\_HDM-Nachricht "SETBITMAPMARGIN"

Legt die Breite des in Pixel angegebenen Rands einer Bitmap in einem vorhandenen Headersteuersatz fest. Sie können diese Nachricht explizit senden oder das [**\_ Header-Makro SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die in Pixel angegebene Breite des Rands, der eine Bitmap innerhalb eines vorhandenen Header-Steuerelements umgibt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Breite des Bitmaprands in Pixel zurück. Wenn der Bitmaprand nicht zuvor angegeben wurde, wird der Standardwert 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

