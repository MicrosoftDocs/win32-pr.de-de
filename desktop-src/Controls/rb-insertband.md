---
title: RB_INSERTBAND Meldung (kommstrg. h)
description: Fügt ein neues Band in ein Grund leisten-Steuerelement ein.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Windows-Steuerelemente für RB_INSERTBAND Meldung
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
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859336"
---
# <a name="rb_insertband-message"></a>RB \_ InsertBand-Nachricht

Fügt ein neues Band in ein Grund leisten-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Position, an der das Band eingefügt wird. Wenn Sie diesen Parameter auf "-1" festlegen, fügt das Steuerelement das neue Band am letzten Speicherort hinzu.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur, die das einzufügende Band definiert. Sie müssen den **CBSIZE** -Member dieser Struktur auf **sizeof**(REBARBANDINFO) festlegen, bevor Sie diese Nachricht senden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **RB \_ Insertbandw** (Unicode) und **RB \_ insertbanda** (ANSI)<br/>               |



 

 





