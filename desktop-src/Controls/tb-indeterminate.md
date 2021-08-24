---
title: TB_INDETERMINATE-Nachricht (Commctrl.h)
description: Legt den unbestimmten Zustand der angegebenen Schaltfläche auf einer Symbolleiste fest oder löscht sie.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90845f269d0af1e690d5ddeb02f2a8ec2a2f63ff4f698f1dd0f3e2729d98b72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078264"
---
# <a name="tb_indeterminate-message"></a>TB \_ INDETERMINATE-Nachricht

Legt den unbestimmten Zustand der angegebenen Schaltfläche auf einer Symbolleiste fest oder löscht sie.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche, deren unbestimmter Zustand festgelegt oder gelöscht werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist eine **BOOL,** die angibt, ob der unbestimmte Zustand festgelegt oder gelöscht werden soll. True gibt an, dass der unbestimmte Zustand festgelegt ist. False gibt an, dass der Zustand gelöscht wird.

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

