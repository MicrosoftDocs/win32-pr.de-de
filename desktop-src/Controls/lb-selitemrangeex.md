---
title: LB_SELITEMRANGEEX Meldung (Winuser. h)
description: Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl aus.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Windows-Steuerelemente für LB_SELITEMRANGEEX Meldung
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956999"
---
# <a name="lb_selitemrangeex-message"></a>LB- \_ selitemrangeex-Nachricht

Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index des ersten Elements an, das ausgewählt werden soll.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den NULL basierten Index des letzten Elements an, das ausgewählt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Wenn der *wParam* -Parameter kleiner als der *LPARAM* -Parameter ist, wird der angegebene Bereich von Elementen ausgewählt. Wenn *wParam* größer oder gleich *LPARAM* ist, wird der Bereich aus dem angegebenen Bereich von Elementen entfernt. Um nur ein Element auszuwählen, wählen Sie zwei Elemente aus, und deaktivieren Sie dann das unerwünschte Element.

Verwenden Sie diese Meldung nur für Listenfelder mit Mehrfachauswahl.

Diese Meldung kann einen Bereich nur innerhalb der ersten 65.536 Elemente auswählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**LB- \_ selitemrange**](lb-selitemrange.md)
</dt> <dt>

[**LB- \_ Sekunden**](lb-setsel.md)
</dt> </dl>

 

 





