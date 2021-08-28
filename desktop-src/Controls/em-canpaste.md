---
title: EM_CANPASTE (Richedit.h)
description: Bestimmt, ob ein Rich-Edit-Steuerelement ein angegebenes Zwischenablageformat einfügen kann.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE der Windows Steuerelemente
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f2d831cd3b3d04fcb7859d2b5936b7354fbb6b638558d605c9f8c5a6ee6333
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916060"
---
# <a name="em_canpaste-message"></a>EM \_ CANPASTE-Nachricht

Bestimmt, ob ein Rich-Edit-Steuerelement ein angegebenes Zwischenablageformat einfügen kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die [auszuprobierenden Zwischenablageformate](/windows/desktop/dataxchg/clipboard-formats) an. Legen Sie diesen Parameter auf 0 (null) fest, um ein beliebiges Format zu testen, das sich derzeit in der Zwischenablage befindet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Zwischenablageformat eingefügt werden kann, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn das Format der Zwischenablage nicht eingefügt werden kann, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

