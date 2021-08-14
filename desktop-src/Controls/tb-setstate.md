---
title: TB_SETSTATE (Commctrl.h)
description: Legt den Zustand für die angegebene Schaltfläche in einer Symbolleiste fest.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9ee112e4bbbe9c64ceab6205d67ecd6ae9653df97be55991be38eb5d181d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167470"
---
# <a name="tb_setstate-message"></a>TB \_ SETSTATE-Nachricht

Legt den Zustand für die angegebene Schaltfläche in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine Kombination von Werten, die unter Symbolleisten-Schaltflächenzustände [aufgeführt sind.](toolbar-button-states.md) Das [**HIWORD muss**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

