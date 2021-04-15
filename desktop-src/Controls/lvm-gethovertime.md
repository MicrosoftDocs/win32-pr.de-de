---
title: LVM_GETHOVERTIME Meldung (kommstrg. h)
description: Ruft die Zeitspanne ab, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView \_ gethovertime-Makro verwenden.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Windows-Steuerelemente für LVM_GETHOVERTIME Meldung
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477574"
---
# <a name="lvm_gethovertime-message"></a>LVM- \_ gethovertime-Nachricht

Ruft die Zeitspanne ab, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ gethovertime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeitspanne in Millisekunden zurück, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Wenn der Rückgabewert (**DWORD**)-1 ist, ist die Hover-Zeit die standardmäßige Hover-Zeit.

## <a name="remarks"></a>Bemerkungen

Die Hover-Zeit wirkt sich nur auf Listenansicht-Steuerelemente aus, die über die [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md)-, [**LVS \_ Ex \_ oneclickreaktivierungs**](extended-list-view-styles.md)-oder [**LVS \_ Ex \_ twoclickaktivierungs**](extended-list-view-styles.md) -Stil der erweiterten Listenansicht verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





