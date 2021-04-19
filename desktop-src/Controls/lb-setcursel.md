---
title: LB_SETCURSEL Meldung (Winuser. h)
description: Wählt eine Zeichenfolge aus und führt ggf. einen Bildlauf in die Ansicht aus. Wenn die neue Zeichenfolge ausgewählt ist, wird die Hervorhebung im Listenfeld aus der zuvor ausgewählten Zeichenfolge entfernt.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Windows-Steuerelemente für LB_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344702"
---
# <a name="lb_setcursel-message"></a>LB- \_ setcurrsel-Nachricht

Wählt eine Zeichenfolge aus und führt ggf. einen Bildlauf in die Ansicht aus. Wenn die neue Zeichenfolge ausgewählt ist, wird die Hervorhebung im Listenfeld aus der zuvor ausgewählten Zeichenfolge entfernt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index der ausgewählten Zeichenfolge an. Wenn dieser Parameter-1 ist, wird für das Listenfeld festgelegt, dass keine Auswahl vorhanden ist.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err. Wenn der *wParam* -Parameter-1 ist, ist der Rückgabewert "lb err", obwohl \_ kein Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung nur für Listenfelder mit einfacher Auswahl. Sie können Sie nicht verwenden, um eine Auswahl in einem Listenfeld mit Mehrfachauswahl festzulegen oder zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ getcurrsel**](lb-getcursel.md)
</dt> </dl>

 

 





