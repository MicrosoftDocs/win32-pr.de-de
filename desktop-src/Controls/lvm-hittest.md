---
title: LVM_HITTEST (Commctrl.h)
description: Bestimmt, welches Listenansichtselement sich an einer angegebenen Position befindet, sofern eines davon ist. Sie können diese Nachricht explizit oder mithilfe des ListView \_ HitTest-Makros senden.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958169"
---
# <a name="lvm_hittest-message"></a>\_LVM-HITTEST-Nachricht

Bestimmt, welches Listenansichtselement sich an einer angegebenen Position befindet, sofern eines davon ist. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ HitTest-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss den Wert 0 (null) haben. **Windows Vista.** Sollte -1 sein, wenn die **iGroup-** und **iSubItem-Member** der *lParam-Struktur* abgerufen werden sollen.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVHITTESTINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) die die Position des Treffertests enthält und Informationen zu den Ergebnissen des Treffertests empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements an der angegebenen Position zurück, sofern dies der Fall ist, oder -1 andernfalls .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





