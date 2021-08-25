---
title: DTM_GETDATETIMEPICKERINFO (Commctrl.h)
description: Ruft Informationen zu einem DTP-Steuerelement (Date and Time Picker) ab.
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48dc639a48455564b9f925f7d6eea9634c01e597323f81d951cfde372a34ea37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878220"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>SMS \_ GETDATETIMEPICKERINFO-Meldung

Ruft Informationen zu einem DTP-Steuerelement (Date and Time Picker) ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd> Ein Zeiger auf <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO,**</a> um die Informationen zu empfangen. Der Aufrufer ist für die Zuweisung des Arbeitsspeichers für diese Struktur verantwortlich. Legen Sie **den cbSize-Member** der -Struktur auf sizeof(DATETIMEPICKERINFO) fest, bevor Sie diese Nachricht senden.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





