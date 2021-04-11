---
title: LB_SETANCHORINDEX Meldung (Winuser. h)
description: Legt das Anker Element \ 8212 fest, d. h. das Element, aus dem eine Mehrfachauswahl beginnt. Eine Mehrfachauswahl umfasst alle Elemente vom Anker Element bis zum Caretzeichen.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Windows-Steuerelemente für LB_SETANCHORINDEX Meldung
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105537"
---
# <a name="lb_setanchorindex-message"></a>LB- \_ Nachricht

Legt das Anker Element fest, das das Element ist, aus dem eine Mehrfachauswahl beginnt. Eine Mehrfachauswahl umfasst alle Elemente vom Anker Element bis zum Caretzeichen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Index des neuen Anker Elements an.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Meldung fehlschlägt, ist der Rückgabewert lb \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ getanchorindex**](lb-getanchorindex.md)
</dt> </dl>

 

 





