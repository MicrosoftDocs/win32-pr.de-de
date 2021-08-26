---
title: CB_DELETESTRING Nachricht (Winuser.h)
description: Löscht eine Zeichenfolge im Listenfeld eines Kombinationsfelds.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0bed1d654b86ffeb4a02c780678822e1999847ef0e163e35ecba081af099f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063580"
---
# <a name="cb_deletestring-message"></a>CB \_ DELETESTRING-Nachricht

Löscht eine Zeichenfolge im Listenfeld eines Kombinationsfelds.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der zu löschenden Zeichenfolge.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der zeichenfolgen, die in der Liste verbleiben. Wenn der *wParam-Parameter* einen Index angibt, der größer als die Anzahl der Elemente in der Liste ist, ist der Rückgabewert CB \_ ERR.

## <a name="remarks"></a>Hinweise

Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil erstellen, jedoch ohne den [**CBS \_ HASSTRINGS-Stil,**](combo-box-styles.md) sendet das System eine [**WM \_ DELETEITEM-Nachricht**](wm-deleteitem.md) an den Besitzer des Kombinationsfelds, damit die Anwendung alle zusätzlichen Daten freigeben kann, die dem Element zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





