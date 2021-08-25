---
title: RB_INSERTBAND (Commctrl.h)
description: Fügt ein neues Band in ein Rebar-Steuerelement ein.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e21020302e4dcbfeb75f4a57d37be4b5c5703668231e8ec8e9dd9bd9577cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770160"
---
# <a name="rb_insertband-message"></a>RB \_ INSERTBAND-Nachricht

Fügt ein neues Band in ein Rebar-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index der Position, an der das Band eingefügt wird. Wenn Sie diesen Parameter auf -1 festlegen, fügt das Steuerelement das neue Band an der letzten Position hinzu.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**REBARBANDINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) die das zu einfügende Band definiert. Sie müssen den **cbSize-Member** dieser -Struktur auf **sizeof**(REBARBANDINFO) festlegen, bevor Sie diese Nachricht senden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **RB \_ INSERTBANDW** (Unicode) und **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





