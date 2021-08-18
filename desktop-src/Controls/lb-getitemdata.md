---
title: LB_GETITEMDATA-Nachricht (Winuser.h)
description: Ruft den anwendungsdefinierte Wert ab, der dem angegebenen Listenfeldelement zugeordnet ist.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA Windows-Steuerelementen
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
ms.openlocfilehash: 1bbfdb091fb98c0cf448af1cf5f554f7d0db2b03f53826154f7d62f2f6b27b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019338"
---
# <a name="lb_getitemdata-message"></a>LB \_ GETITEMDATA-Nachricht

Ruft den anwendungsdefinierte Wert ab, der dem angegebenen Listenfeldelement zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements.

Windows 95/Windows 98/Windows Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Das bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Byte nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Wert, der dem Element zugeordnet ist, oder LB \_ ERR, wenn ein Fehler auftritt. Wenn sich das Element in einem vom Besitzer gezeichneten Listenfeld befindet und ohne den [**LBS \_ HASSTRINGS-Stil**](list-box-styles.md) erstellt wurde, befand sich dieser Wert im *lParam-Parameter* der [**LB \_ ADDSTRING-**](lb-addstring.md) oder [**LB \_ INSERTSTRING-Nachricht,**](lb-insertstring.md) die das Element dem Listenfeld hinzugefügt hat. Andernfalls ist es der Wert in der *lParam* der [**LB \_ SETITEMDATA-Nachricht.**](lb-setitemdata.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
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

[**LB \_ SETITEMDATA**](lb-setitemdata.md)
</dt> </dl>

 

 





