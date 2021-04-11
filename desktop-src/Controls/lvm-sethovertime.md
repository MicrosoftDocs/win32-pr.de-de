---
title: LVM_SETHOVERTIME Meldung (kommstrg. h)
description: Legt den Zeitraum fest, in dem der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView- \_ Makro "-Serverzeit" verwenden.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Windows-Steuerelemente für LVM_SETHOVERTIME Meldung
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
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102886"
---
# <a name="lvm_sethovertime-message"></a>LVM- \_ mesvertime-Nachricht

Legt den Zeitraum fest, in dem der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView-Makro "- [**\_ Serverzeit**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) " verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Die neue Zeitspanne (in Millisekunden), die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Wenn dieser Wert (**DWORD**)-1 ist, wird die Hover-Zeit auf die standardmäßige Hover-Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Hover-Zeit zurück.

## <a name="remarks"></a>Bemerkungen

Die Hover-Zeit wirkt sich nur auf Listenansicht-Steuerelemente aus, die über die [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md)-, [**LVS \_ Ex \_ oneclickreaktivierungs**](extended-list-view-styles.md)-oder [**LVS \_ Ex \_ twoclickaktivierungs**](extended-list-view-styles.md) -Stil der erweiterten Listenansicht verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





