---
title: LB_GETTOPINDEX Meldung (Winuser. h)
description: Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- Windows-Steuerelemente für LB_GETTOPINDEX Meldung
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
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956505"
---
# <a name="lb_gettopindex-message"></a>LB- \_ gettopindex-Nachricht

Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab. Anfänglich befindet sich das Element mit dem Index 0 am oberen Rand des Listen Felds, aber wenn für den Listenfeld Inhalt ein Bildlauf ausgeführt wurde, befindet sich möglicherweise ein anderes Element im oberen Bereich. Das erste sichtbare Element in einem Listenfeld mit mehreren Spalten ist das linke obere Element.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ settopindex**](lb-settopindex.md)
</dt> </dl>

 

 





