---
title: TVM_SETLINECOLOR (Commctrl.h)
description: Die TVM \_ SETLINECOLOR-Meldung legt die aktuelle Linienfarbe fest.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af66e7a711611ff5e59ec0d68b58a24fb39399245437b0e5d81840c1c38b2d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669520"
---
# <a name="tvm_setlinecolor-message"></a>TVM \_ SETLINECOLOR-Meldung

Die **TVM \_ SETLINECOLOR-Meldung** legt die aktuelle Linienfarbe fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Linienfarbe. Verwenden Sie den CLR \_ DEFAULT-Wert, um die Standardfarben des Systems wiederherzustellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Zeilenfarbe zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung ändert nur die Linienfarben. Um die Farben von "+" und "-" innerhalb der Schaltflächen zu ändern, verwenden Sie die [**TVM \_ SETTEXTCOLOR-Meldung.**](tvm-settextcolor.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





