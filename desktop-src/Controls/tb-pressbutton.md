---
title: TB_PRESSBUTTON (Commctrl.h)
description: Drückt oder gibt die angegebene Schaltfläche in einer Symbolleiste frei.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c72bd3e58b06510463fcfb872060d7fcbb529ce3e5a96376ae8cb25e142d9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168010"
---
# <a name="tb_pressbutton-message"></a>TB \_ PRESSBUTTON-Meldung

Drückt oder gibt die angegebene Schaltfläche in einer Symbolleiste frei.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche, die gedrückt oder loslasst werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

LoWORD [**ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine **BOOL,** die angibt, ob die angegebene Schaltfläche gedrückt oder losgelassen werden soll. True **gibt an,** dass die Schaltfläche gedrückt wird. False **gibt an,** dass die Schaltfläche freigegeben wird.

Das [**HIWORD muss**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

