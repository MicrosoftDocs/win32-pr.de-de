---
title: CB_SETTOPINDEX Meldung (Winuser. h)
description: Eine Anwendung sendet die CB- \_ settopindex-Nachricht, um sicherzustellen, dass ein bestimmtes Element im Listenfeld eines Kombinations Felds sichtbar ist.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Windows-Steuerelemente für CB_SETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740120"
---
# <a name="cb_settopindex-message"></a>CB \_ settopindex-Meldung

Eine Anwendung sendet die **CB- \_ settopindex** -Nachricht, um sicherzustellen, dass ein bestimmtes Element im Listenfeld eines Kombinations Felds sichtbar ist. Das System führt einen Bildlauf im Listenfeld Inhalt durch, sodass entweder das angegebene Element oben im Listenfeld angezeigt wird oder der maximale Bild Laufbereich erreicht wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index des Listen Elements an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ gettopindex**](cb-gettopindex.md)
</dt> </dl>

 

 





