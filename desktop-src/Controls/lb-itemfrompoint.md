---
title: LB_ITEMFROMPOINT Meldung (Winuser. h)
description: Ruft den NULL basierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten liegt.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Windows-Steuerelemente für LB_ITEMFROMPOINT Meldung
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
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743024"
---
# <a name="lb_itemfrompoint-message"></a>LB- \_ itemfrompoint-Nachricht

Ruft den NULL basierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten liegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die x-Koordinate eines Punkts relativ zur oberen linken Ecke des Client Bereichs des Listen Felds an.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die y-Koordinate eines Punkts relativ zur oberen linken Ecke des Client Bereichs des Listen Felds an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert enthält den Index des nächstgelegenen Elements im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist 0 (null), wenn sich der angegebene Punkt im Client Bereich des Listen Felds befindet, oder eines, wenn es außerhalb des Client Bereichs liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Makelparam**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

