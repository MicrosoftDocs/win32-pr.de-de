---
title: TB_HIDEBUTTON Meldung (kommstrg. h)
description: Blendet die angegebene Schaltfläche in einer Symbolleiste ein oder aus.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- Windows-Steuerelemente für TB_HIDEBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949698"
---
# <a name="tb_hidebutton-message"></a>TB- \_ hidebutton-Meldung

Blendet die angegebene Schaltfläche in einer Symbolleiste ein oder aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Befehls Bezeichner der Schaltfläche, die ausgeblendet oder angezeigt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche ausgeblendet oder angezeigt werden soll. **True** gibt an, dass die Schaltfläche ausgeblendet ist. Wenn der Wert **false** ist, wird die Schaltfläche angezeigt.

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



 

