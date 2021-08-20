---
title: TB_MARKBUTTON (Commctrl.h)
description: Legt den Hervorhebungszustand einer angegebenen Schaltfläche in einem Symbolleisten-Steuerelement fest.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- TB_MARKBUTTON meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af7ba20ed9ce3d1b289c0c28db8fc40c476dd99f4ffb1af1af28692c44cab1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168026"
---
# <a name="tb_markbutton-message"></a>TB \_ MARKBUTTON-Nachricht

Legt den Hervorhebungszustand einer angegebenen Schaltfläche in einem Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner für eine Symbolleistenschaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>

LoWORD [**ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine **BOOL,** die den neuen Hervorhebungszustand angibt. True **gibt an,** dass die Schaltfläche hervorgehoben ist. False **gibt an,** dass die Schaltfläche auf ihren Standardzustand festgelegt ist.

Das [**HIWORD muss**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

