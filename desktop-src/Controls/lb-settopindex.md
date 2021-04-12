---
title: LB_SETTOPINDEX Meldung (Winuser. h)
description: Stellt sicher, dass das angegebene Element in einem Listenfeld sichtbar ist.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- Windows-Steuerelemente für LB_SETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105524"
---
# <a name="lb_settopindex-message"></a>LB- \_ settopindex-Meldung

Stellt sicher, dass das angegebene Element in einem Listenfeld sichtbar ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Elements im Listenfeld.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Das System führt einen Bildlauf im Listenfeld Inhalt durch, sodass entweder das angegebene Element oben im Listenfeld angezeigt wird oder der maximale Bild Laufbereich erreicht wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ gettopindex**](lb-gettopindex.md)
</dt> </dl>

 

 





