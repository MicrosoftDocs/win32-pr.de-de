---
title: LVM_INSERTGROUP (Commctrl.h)
description: Fügt eine Gruppe in ein Listenansicht-Steuerelement ein.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP von Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31504226663b0df91e0297ed29abf784ff239dfcee5f323e8617f73dff65acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019248"
---
# <a name="lvm_insertgroup-message"></a>LVM \_ INSERTGROUP-Nachricht

Fügt eine Gruppe in ein Listenansicht-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Index, an dem die Gruppe hinzugefügt werden soll. Wenn dies -1 ist, wird die Gruppe am Ende der Liste hinzugefügt.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP-Struktur,**</a> die die hinzuzufügende Gruppe enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, dem die Gruppe hinzugefügt wurde, oder -1, wenn der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Um den Gruppenmodus zu aktivieren, rufen [**Sie LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) oder [**ListView \_ EnableGroupView auf.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)

Eine Gruppe kann nicht in ein leeres Listenansicht-Steuerelement eingefügt werden.

Stellen Sie sicher, dass **Sie die iGroupId** in den Element(en) festlegen, dem die Gruppe hinzugefügt wurde. Andernfalls zeigt das ListView-Steuerelement nach der Verarbeitung von [**LVM \_ ENABLEGROUPVIEW-Nachrichten**](lvm-enablegroupview.md) mit **TRUE** keine Elemente an.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32 Version 6.0 ankn.0 ankn.) Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





