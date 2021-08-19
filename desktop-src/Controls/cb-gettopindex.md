---
title: CB_GETTOPINDEX (Winuser.h)
description: Eine Anwendung sendet die CB GETTOPINDEX-Nachricht, um den nullbasierten Index des ersten sichtbaren Elements im Listenfeldteil eines \_ Kombinationsfelds abzurufen.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2360b07c86d6d5bcbb8296d705e8ef65b3a81481a8fc647a362aedc729f38b42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089110"
---
# <a name="cb_gettopindex-message"></a>CB \_ GETTOPINDEX-Nachricht

Eine Anwendung sendet die **CB \_ GETTOPINDEX-Nachricht,** um den nullbasierten Index des ersten sichtbaren Elements im Listenfeldteil eines Kombinationsfelds abzurufen. Anfänglich befindet sich das Element mit index 0 oben im Listenfeld, aber wenn der Inhalt des Listenfelds gescrollt wurde, befindet sich möglicherweise ein anderes Element oben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der Index des ersten sichtbaren Elements im Listenfeld des Kombinationsfelds.

Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ ERR.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ SETTOPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 





