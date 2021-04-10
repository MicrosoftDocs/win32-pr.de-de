---
title: HDM_GETBITMAPMARGIN Meldung (kommstrg. h)
description: Ruft die Breite des bitmaprandes für ein Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ getbitmapmargin-Makro verwenden.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Windows-Steuerelemente für HDM_GETBITMAPMARGIN Meldung
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956508"
---
# <a name="hdm_getbitmapmargin-message"></a>HDM \_ getbitmapmargin-Meldung

Ruft die Breite des bitmaprandes für ein Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das- [**Header \_ getbitmapmargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Breite des bitmaprandes in Pixel zurück. Wenn der bitmaprand zuvor nicht angegeben wurde, wird der Standardwert 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ cxedge) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HDM \_ setbitmapmargin**](hdm-setbitmapmargin.md)
</dt> </dl>

 

