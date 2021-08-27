---
title: LB_GETTOPINDEX (Winuser.h)
description: Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b23360da45041e5a728f370e54f8250f216507dd439291a2ffce5ed383d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085380"
---
# <a name="lb_gettopindex-message"></a>LB \_ GETTOPINDEX-Nachricht

Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab. Anfänglich befindet sich das Element mit index 0 oben im Listenfeld, aber wenn der Inhalt des Listenfelds gescrollt wurde, befindet sich möglicherweise ein anderes Element oben. Das erste sichtbare Element in einem Listenfeld mit mehreren Spalten ist das element oben links.

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

Der Rückgabewert ist der Index des ersten sichtbaren Elements im Listenfeld.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB \_ SETTOPINDEX**](lb-settopindex.md)
</dt> </dl>

 

 





