---
title: CB_GETTOPINDEX Meldung (Winuser. h)
description: Eine Anwendung sendet die CB \_ gettopindex-Nachricht, um den NULL basierten Index des ersten sichtbaren Elements im Listenfeld Teil eines Kombinations Felds abzurufen.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Windows-Steuerelemente für CB_GETTOPINDEX Meldung
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
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956452"
---
# <a name="cb_gettopindex-message"></a>CB \_ gettopindex-Meldung

Eine Anwendung sendet die **CB \_ gettopindex** -Nachricht, um den NULL basierten Index des ersten sichtbaren Elements im Listenfeld Teil eines Kombinations Felds abzurufen. Anfänglich befindet sich das Element mit dem Index 0 am oberen Rand des Listen Felds, aber wenn für den Listenfeld Inhalt ein Bildlauf ausgeführt wurde, befindet sich möglicherweise ein anderes Element im oberen Bereich.

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

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der Index des ersten sichtbaren Elements im Listenfeld des Kombinations Felds.

Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ settopindex**](cb-settopindex.md)
</dt> </dl>

 

 





