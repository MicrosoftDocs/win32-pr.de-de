---
title: HDM_SETORDERARRAY Meldung (kommstrg. h)
description: Legt die Reihenfolge von Header Elementen von links nach rechts fest. Sie können diese Nachricht explizit senden oder das Header- \_ /s--Makro-Makro verwenden.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Windows-Steuerelemente für HDM_SETORDERARRAY Meldung
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476974"
---
# <a name="hdm_setorderarray-message"></a>HDM- \_ Nachricht "abderarray"

Legt die Reihenfolge von Header Elementen von links nach rechts fest. Sie können diese Nachricht explizit senden oder das [**Header- \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) /s--Makro-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Größe des Puffers bei *LPARAM* in-Elementen. Dieser Wert muss mit dem von [**HDM \_ GetItemCount**](hdm-getitemcount.md)zurückgegebenen Wert identisch sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array, das die Reihenfolge angibt, in der Elemente angezeigt werden sollen, von links nach rechts. Wenn der Inhalt des-Arrays beispielsweise {2,0,1} ist, zeigt das-Steuerelement Element 2, Element 0 und Element 1 von links nach rechts an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





