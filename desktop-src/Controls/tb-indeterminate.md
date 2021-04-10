---
title: TB_INDETERMINATE Meldung (kommstrg. h)
description: Legt den unbestimmten Zustand der angegebenen Schaltfläche in einer Symbolleiste fest oder löscht ihn.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- Windows-Steuerelemente für TB_INDETERMINATE Meldung
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
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040433"
---
# <a name="tb_indeterminate-message"></a>TB \_ unbestimmte Nachricht

Legt den unbestimmten Zustand der angegebenen Schaltfläche in einer Symbolleiste fest oder löscht ihn.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehls Bezeichner der Schaltfläche, deren unbestimmter Zustand festgelegt oder gelöscht werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob der unbestimmte Zustand festgelegt oder gelöscht werden soll. **True** gibt an, dass der unbestimmte Zustand festgelegt wird. Wenn der Wert **false** ist, wird der Status gelöscht.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

