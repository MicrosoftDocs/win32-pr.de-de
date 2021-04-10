---
title: LB_SETCOUNT Meldung (Winuser. h)
description: Legt die Anzahl von Elementen in einem Listenfeld fest, das mit dem lbs \_ NODATA-Stil erstellt wurde und nicht mit dem lbs \_ hasstrings-Stil erstellt wurde.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Windows-Steuerelemente für LB_SETCOUNT Meldung
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040893"
---
# <a name="lb_setcount-message"></a>LB- \_ SetCount-Nachricht

Legt die Anzahl von Elementen in einem Listenfeld fest, das mit dem [**lbs \_ NODATA**](list-box-styles.md) -Stil erstellt wurde und nicht mit dem [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die neue Anzahl von Elementen im Listenfeld an.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err. Wenn nicht genügend Arbeitsspeicher zum Speichern der Elemente vorhanden ist, lautet der Rückgabewert "lb \_ errspace".

## <a name="remarks"></a>Bemerkungen

Die **lb- \_ SetCount** -Nachricht wird nur von Listenfeldern unterstützt, die mit dem [**lbs \_ NODATA**](list-box-styles.md) -Stil erstellt wurden und nicht mit dem [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurden. Alle anderen Listenfelder geben lb- \_ Err zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ GetCount**](lb-getcount.md)
</dt> </dl>

 

 





