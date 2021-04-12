---
title: LB_SETITEMDATA Meldung (Winuser. h)
description: Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Windows-Steuerelemente für LB_SETITEMDATA Meldung
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105531"
---
# <a name="lb_setitemdata-message"></a>LB- \_ Nachricht

Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index des Elements an. Wenn dieser Wert-1 ist, gilt der *LPARAM* -Wert für alle Elemente im Listenfeld.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den Wert an, der dem Element zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Wenn sich das Element in einem von einem Besitzer gezeichneten Listenfeld befindet, das ohne den [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde, ersetzt diese Nachricht den Wert, der im *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht enthalten ist, die das Element dem Listenfeld hinzugefügt hat.

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

[**LB- \_ AddString**](lb-addstring.md)
</dt> <dt>

[**LB- \_ GetItemData**](lb-getitemdata.md)
</dt> <dt>

[**LB- \_ InsertString**](lb-insertstring.md)
</dt> </dl>

 

 





