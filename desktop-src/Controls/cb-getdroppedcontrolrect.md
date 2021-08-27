---
title: CB_GETDROPPEDCONTROLRECT-Nachricht (Winuser.h)
description: Eine Anwendung sendet eine CB \_ GETDROPPEDCONTROLRECT-Nachricht, um die Bildschirmkoordinaten eines Kombinationsfelds im abgelegten Zustand abzurufen.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: c140abb139cc47020f333ccf66f71cf36d890449be91d66f51b646db22091c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089280"
---
# <a name="cb_getdroppedcontrolrect-message"></a>CB \_ GETDROPPEDCONTROLRECT-Nachricht

Eine Anwendung sendet eine **CB \_ GETDROPPEDCONTROLRECT-Nachricht,** um die Bildschirmkoordinaten eines Kombinationsfelds im abgelegten Zustand abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die RECT-Struktur, die die Koordinaten des Kombinationsfelds im abgelegten Zustand [**empfängt.**](/previous-versions//dd162897(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert ungleich 0 (null).

Wenn die Nachricht fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

