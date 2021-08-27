---
title: IPM_SETFOCUS (Commctrl.h)
description: Legt den Tastaturfokus auf das angegebene Feld im IP-Adresssteuerfeld fest. Der ganze Text in diesem Feld wird ausgewählt.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS meldungssteuerelemente Windows
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
ms.openlocfilehash: 2a74d98aa4d4259d11d7fef6e0bfdad2bfe741447ddffab27fa41545e7eda515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085570"
---
# <a name="ipm_setfocus-message"></a>IPM \_ SETFOCUS-Nachricht

Legt den Tastaturfokus auf das angegebene Feld im IP-Adresssteuerfeld fest. Der ganze Text in diesem Feld wird ausgewählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein nullbasierter Feldindex, auf den der Fokus festgelegt werden soll. Wenn dieser Wert größer als die Anzahl der Felder ist, wird der Fokus auf das erste leere Feld festgelegt. Wenn alle Felder nicht verfügbar sind, wird der Fokus auf das erste Feld festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





