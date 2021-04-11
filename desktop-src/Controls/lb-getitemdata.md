---
title: LB_GETITEMDATA Meldung (Winuser. h)
description: Ruft den Anwendungs definierten Wert ab, der dem angegebenen Listenfeld Element zugeordnet ist.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Windows-Steuerelemente für LB_GETITEMDATA Meldung
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105992"
---
# <a name="lb_getitemdata-message"></a>LB- \_ GetItemData-Nachricht

Ruft den Anwendungs definierten Wert ab, der dem angegebenen Listenfeld Element zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Wert, der dem Element zugeordnet ist, oder lb \_ Err, wenn ein Fehler auftritt. Wenn sich das Element in einem vom Besitzer gezeichneten Listenfeld befindet und ohne den [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde, war dieser Wert im *LPARAM* -Parameter der [**lb- \_ AddString**](lb-addstring.md) -oder der [**lb- \_ InsertString**](lb-insertstring.md) -Nachricht enthalten, die das Element dem Listenfeld hinzugefügt hat. Andernfalls ist es der Wert im *LPARAM* der LB-Nachricht [**\_**](lb-setitemdata.md) .

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

[**LB- \_ InsertString**](lb-insertstring.md)
</dt> <dt>

[**LB- \_ Daten**](lb-setitemdata.md)
</dt> </dl>

 

 





