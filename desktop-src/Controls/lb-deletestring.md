---
title: LB_DELETESTRING Meldung (Winuser. h)
description: Löscht eine Zeichenfolge in einem Listenfeld.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Windows-Steuerelemente für LB_DELETESTRING Meldung
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859126"
---
# <a name="lb_deletestring-message"></a>LB- \_ deletestring-Nachricht

Löscht eine Zeichenfolge in einem Listenfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der zu löschenden Zeichenfolge.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der Zeichen folgen, die in der Liste verbleiben. Der Rückgabewert ist lb \_ Err, wenn der *wParam* -Parameter einen Index angibt, der größer als die Anzahl der Elemente in der Liste ist.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung das Listenfeld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt, sendet das System eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung an den Besitzer des Listen Felds, sodass die Anwendung alle zusätzlichen Daten freigibt, die dem Element zugeordnet sind.

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

[**WM- \_ DeleteItem**](wm-deleteitem.md)
</dt> </dl>

 

 





