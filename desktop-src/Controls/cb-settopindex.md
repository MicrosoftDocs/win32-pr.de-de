---
title: CB_SETTOPINDEX (Winuser.h)
description: Eine Anwendung sendet die CB SETTOPINDEX-Nachricht, um sicherzustellen, dass ein bestimmtes Element im Listenfeld \_ eines Kombinationsfelds sichtbar ist.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX von Windows-Steuerelementen
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
ms.openlocfilehash: d9364ef5013ef692adda76f96752f11691d5f4cc87c857386914105d16decb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832288"
---
# <a name="cb_settopindex-message"></a>CB \_ SETTOPINDEX-Meldung

Eine Anwendung sendet die **CB \_ SETTOPINDEX-Nachricht,** um sicherzustellen, dass ein bestimmtes Element im Listenfeld eines Kombinationsfelds sichtbar ist. Das System führt einen Bildlauf durch den Inhalt des Listenfelds durch, sodass entweder das angegebene Element oben im Listenfeld angezeigt wird oder der maximale Bildlaufbereich erreicht wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den nullbasierten Index des Listenelements an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ ERR.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CB \_ GETTOPINDEX**](cb-gettopindex.md)
</dt> </dl>

 

 





