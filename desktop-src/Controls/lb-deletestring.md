---
title: LB_DELETESTRING (Winuser.h)
description: Löscht eine Zeichenfolge in einem Listenfeld.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING meldungssteuerelemente Windows
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
ms.openlocfilehash: 3329f82babea73a6392f7c360623fdeadec843dfcfd62e70106e7fb1cb0367ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671675"
---
# <a name="lb_deletestring-message"></a>LB \_ DELETESTRING-Meldung

Löscht eine Zeichenfolge in einem Listenfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der zu löschenden Zeichenfolge.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der in der Liste verbleibenden Zeichenfolgen. Der Rückgabewert ist LB \_ ERR, wenn der *wParam-Parameter* einen Index angibt, der größer als die Anzahl der Elemente in der Liste ist.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung das Listenfeld mit einem vom Besitzer gezeichneten Stil erstellt, aber ohne [**den LBS \_ HASSTRINGS-Stil,**](list-box-styles.md) sendet das System eine [**WM \_ DELETEITEM-Nachricht**](wm-deleteitem.md) an den Besitzer des Listenfelds, damit die Anwendung alle zusätzlichen Daten, die dem Element zugeordnet sind, frei geben kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





