---
title: LB_GETSELITEMS Meldung (Winuser. h)
description: Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Element Nummern ausgewählter Elemente in einem Listenfeld mit Mehrfachauswahl angeben.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Windows-Steuerelemente für LB_GETSELITEMS Meldung
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956542"
---
# <a name="lb_getselitems-message"></a>LB- \_ getselitems-Nachricht

Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Element Nummern ausgewählter Elemente in einem Listenfeld mit Mehrfachauswahl angeben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl ausgewählter Elemente, deren Element Nummer in den Puffer eingefügt werden soll.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der groß genug für die Anzahl der vom *wParam* -Parameter angegebenen ganzzahligen Werte ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der Elemente, die im Puffer abgelegt werden. Wenn das Listenfeld ein Listenfeld für die einfache Auswahl ist, lautet der Rückgabewert lb \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ getselcount**](lb-getselcount.md)
</dt> </dl>

 

 





