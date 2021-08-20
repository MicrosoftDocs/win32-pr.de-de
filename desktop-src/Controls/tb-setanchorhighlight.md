---
title: TB_SETANCHORHIGHLIGHT Meldung (Commctrl.h)
description: Legt die Einstellung für die Ankermarkierung für eine Symbolleiste fest.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a66193aebee80a2ffde97b7e802b5bab750f0a9e2f1773b32d872211d52150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167983"
---
# <a name="tb_setanchorhighlight-message"></a>TB \_ SETANCHORHIGHLIGHT-Meldung

Legt die Einstellung für die Ankermarkierung für eine Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**BOOL-Wert,** der angibt, ob die Ankerhervorhebung aktiviert oder deaktiviert ist. Wenn dieser Wert ungleich 0 (null) ist, wird die Ankerhervorhebung aktiviert. Wenn dieser Wert 0 (null) ist, wird die Ankerhervorhebung deaktiviert.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Einstellung für die Ankermarkierung zurück. Wenn dieser Wert ungleich 0 (null) ist, wurde die Ankerhervorhebung aktiviert. Wenn dieser Wert 0 (null) ist, wurde die Ankerhervorhebung deaktiviert.

## <a name="remarks"></a>Hinweise

Ankerhervorhebung in einer Symbolleiste bedeutet, dass das letzte hervorgehobene Element hervorgehoben bleibt, bis ein anderes Element hervorgehoben wird. Dies tritt auch dann auf, wenn der Cursor das Symbolleistensteuerelement verlässt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





