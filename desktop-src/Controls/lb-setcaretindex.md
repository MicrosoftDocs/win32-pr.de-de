---
title: LB_SETCARETINDEX Meldung (Winuser. h)
description: Legt das Fokus Rechteck auf das Element am angegebenen Index in einem Mehrfachauswahl-Listenfeld fest. Wenn das Element nicht sichtbar ist, wird es in die Ansicht gescrollt.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Windows-Steuerelemente für LB_SETCARETINDEX Meldung
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859164"
---
# <a name="lb_setcaretindex-message"></a>LB- \_ setcaretindex-Meldung

Legt das Fokus Rechteck auf das Element am angegebenen Index in einem Mehrfachauswahl-Listenfeld fest. Wenn das Element nicht sichtbar ist, wird es in die Ansicht gescrollt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index des Listenfeld Elements an, das das Fokus Rechteck erhalten soll.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn dieser Wert **false** ist, wird das Element gescrollt, bis es vollständig sichtbar ist. Wenn der Wert **true** ist, wird das Element so lange gescrollt, bis es mindestens teilweise sichtbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err (-1). Andernfalls wird der Lastenausgleich OK \_ (0) zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn diese Meldung an ein Listenfeld mit einer Auswahl gesendet wird, das kein ausgewähltes Element enthält, wird der Einfügeindex auf das vom *wParam* -Parameter angegebene Element festgelegt. Wenn das Listenfeld für die Einzel Auswahl ein ausgewähltes Element enthält, gibt das Listenfeld lb \_ Err zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB \_ getcaretindex**](lb-getcaretindex.md)
</dt> </dl>

 

 





