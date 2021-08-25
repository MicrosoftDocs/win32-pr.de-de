---
title: LVM_GETHOVERTIME Meldung (Commctrl.h)
description: Ruft die Zeitspanne ab, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView \_ GetHoverTime-Makro verwenden.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 150a8eff54f8b3c27f0e7783ceda67af60c326e370d1a518d83e6bdd214fb529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920100"
---
# <a name="lvm_gethovertime-message"></a>LVM \_ GETHOVERTIME-Nachricht

Ruft die Zeitspanne ab, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ GetHoverTime-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeitspanne in Millisekunden zurück, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Wenn der Rückgabewert (**DWORD**)-1 ist, ist die Hoverzeit die Standardzeigerzeit.

## <a name="remarks"></a>Hinweise

Die Hoverzeit wirkt sich nur auf Listenansichtssteuerelemente aus, die den erweiterten Listenansichtsstil [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)oder [**LVS EX \_ \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





