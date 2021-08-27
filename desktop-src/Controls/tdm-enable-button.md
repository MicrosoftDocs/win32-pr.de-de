---
title: TDM_ENABLE_BUTTON Nachricht (Commctrl.h)
description: Aktiviert oder deaktiviert eine Pushschaltfläche in einem Aufgabendialogfeld.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a76603f61f3e27dce8cf7c8f5504457ce5a29a787b3b1f6357c1c519c735854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104650"
---
# <a name="tdm_enable_button-message"></a>TDM ENABLE BUTTON message (TDM \_ \_ ENABLE BUTTON-Meldung)

Aktiviert oder deaktiviert eine Pushschaltfläche in einem Aufgabendialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein **int-Wert,** der die ID der zu aktivierenden oder zu deaktivierenden Pushschaltfläche angibt.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Gibt den Schaltflächenzustand an. Legen Sie auf 0 fest, um die Schaltfläche zu deaktivieren. legen Sie auf ungleich 0 (null) fest, um die Schaltfläche zu aktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





