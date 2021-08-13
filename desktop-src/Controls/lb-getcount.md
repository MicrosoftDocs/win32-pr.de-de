---
title: LB_GETCOUNT (Winuser.h)
description: Ruft die Anzahl der Elemente in einem Listenfeld ab.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4f4792bf290343e2868b754f8efb1bfc03d0be1f600c9f7584f051053400b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435479"
---
# <a name="lb_getcount-message"></a>LB \_ GETCOUNT-Nachricht

Ruft die Anzahl der Elemente in einem Listenfeld ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der Elemente im Listenfeld oder LB \_ ERR, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

Die zurückgegebene Anzahl ist eins größer als der Indexwert des letzten Elements (der Index ist null-basiert).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**LB \_ SETCOUNT**](lb-setcount.md)
</dt> </dl>

 

 





