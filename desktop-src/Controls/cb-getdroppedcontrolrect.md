---
title: CB_GETDROPPEDCONTROLRECT Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ getdroppedcontrolrect-Nachricht, um die Bildschirm Koordinaten eines Kombinations Felds im Dropdown Zustand abzurufen.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Windows-Steuerelemente für CB_GETDROPPEDCONTROLRECT Meldung
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477334"
---
# <a name="cb_getdroppedcontrolrect-message"></a>CB \_ getdroppedcontrolrect-Meldung

Eine Anwendung sendet eine **CB \_ getdroppedcontrolrect** -Nachricht, um die Bildschirm Koordinaten eines Kombinations Felds im Dropdown Zustand abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des Kombinations Felds im abgehaltenten Zustand empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert ungleich 0 (null).

Wenn die Meldung fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

