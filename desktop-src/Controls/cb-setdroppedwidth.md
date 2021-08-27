---
title: CB_SETDROPPEDWIDTH Meldung (Winuser.h)
description: Eine Anwendung sendet die CB \_ SETDROPPEDWIDTH-Nachricht, um die minimal zulässige Breite des Listenfelds eines Kombinationsfelds im \_ CBS-DROPDOWN- oder \_ CBS-DROPDOWNLIST-Stil in Pixel festzulegen.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d59aee89c4be18ba8e5013fa1a1e685a56b727d293c833c7f99140b683efeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089050"
---
# <a name="cb_setdroppedwidth-message"></a>CB \_ SETDROPPEDWIDTH-Nachricht

Eine Anwendung sendet die **CB \_ SETDROPPEDWIDTH-Nachricht,** um die minimal zulässige Breite des Listenfelds eines Kombinationsfelds im [**\_ CBS-DROPDOWN-**](combo-box-styles.md) oder [**\_ CBS-DROPDOWNLIST-Stil**](combo-box-styles.md) in Pixel festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die minimal zulässige Breite des Listenfelds in Pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Meldung erfolgreich ist, entspricht der Rückgabewert der neuen Breite des Listenfelds.

Wenn die Nachricht fehlschlägt, lautet der Rückgabewert CB \_ ERR.

## <a name="remarks"></a>Hinweise

Standardmäßig ist die zulässige Mindestbreite des Dropdownlistenfelds 0 (null). Die Breite des Listenfelds ist entweder die mindestens zulässige Breite oder die Breite des Kombinationsfelds, je nachdem, welcher Wert größer ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ GETDROPPEDWIDTH**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





