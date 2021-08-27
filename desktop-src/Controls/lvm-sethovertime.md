---
title: LVM_SETHOVERTIME (Commctrl.h)
description: Legt die Zeit fest, die der Mauszeiger auf ein Element bewegen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView \_ SetHoverTime-Makro verwenden.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f93edf917dc50384f3a09f7eadf013561715735a995c63a695cb8f9ad91dbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077230"
---
# <a name="lvm_sethovertime-message"></a>LVM \_ SETHOVERTIME-Meldung

Legt die Zeit fest, die der Mauszeiger auf ein Element bewegen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ SetHoverTime-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Die neue Zeit in Millisekunden, die der Mauszeiger auf ein Element bewegen muss, bevor es ausgewählt wird. Wenn dieser Wert (**DWORD**)-1 ist, wird die Hoverzeit auf die Standardmäßige Hoverzeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Hoverzeit zurück.

## <a name="remarks"></a>Hinweise

Die Hoverzeit wirkt sich nur auf Listenansichtssteuerelemente aus, die den erweiterten Listenansichtsstil [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)oder [**LVS EX \_ \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) haben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





