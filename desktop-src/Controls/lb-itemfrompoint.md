---
title: LB_ITEMFROMPOINT (Winuser.h)
description: Ruft den nullbasierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten ist.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddddd58780cb4b140501c567d699373cb1fa03cbf212332bea71611a4add3788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575930"
---
# <a name="lb_itemfrompoint-message"></a>LB \_ ITEMFROMPOINT-Nachricht

Ruft den nullbasierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die x-Koordinate eines Punkts relativ zur oberen linken Ecke des Clientbereichs des Listenfelds an.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die y-Koordinate eines Punkts relativ zur oberen linken Ecke des Clientbereichs des Listenfelds an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert enthält den Index des nächstgelegenen Elements im [**LOWORD.**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Das [**HIWORD ist**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 0 (null), wenn sich der angegebene Punkt im Clientbereich des Listenfelds befindet, oder ein Punkt, wenn er sich außerhalb des Clientbereichs befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

