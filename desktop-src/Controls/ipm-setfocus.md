---
title: IPM_SETFOCUS Meldung (kommstrg. h)
description: Legt den Tastaturfokus auf das angegebene Feld im IP-Adress Steuerelement fest. Der gesamte Text in diesem Feld wird ausgewählt.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Windows-Steuerelemente für IPM_SETFOCUS Meldung
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104462"
---
# <a name="ipm_setfocus-message"></a>IPM- \_ SetFocus-Nachricht

Legt den Tastaturfokus auf das angegebene Feld im IP-Adress Steuerelement fest. Der gesamte Text in diesem Feld wird ausgewählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein NULL basierter Feld Index, auf den der Fokus festgelegt werden soll. Wenn dieser Wert größer als die Anzahl der Felder ist, wird der Fokus auf das erste leere Feld festgelegt. Wenn alle Felder nicht leer sind, wird der Fokus auf das erste Feld festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





