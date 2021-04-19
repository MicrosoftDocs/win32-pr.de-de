---
title: LVM_INSERTGROUP Meldung (kommstrg. h)
description: Fügt eine Gruppe in ein Listenansicht-Steuerelement ein.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- Windows-Steuerelemente für LVM_INSERTGROUP Meldung
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
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339580"
---
# <a name="lvm_insertgroup-message"></a>LVM \_ insertgroup-Meldung

Fügt eine Gruppe in ein Listenansicht-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Der Index, an dem die Gruppe hinzugefügt werden soll. Wenn der Wert-1 ist, wird die Gruppe am Ende der Liste hinzugefügt.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**orgroup**</a> -Struktur, die die hinzu zufügende Gruppe enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, dem die Gruppe hinzugefügt wurde, oder-1, wenn der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Bemerkungen

Um den Gruppenmodus zu aktivieren, müssen Sie [**LVM \_ enablegroupview**](lvm-enablegroupview.md) oder [**ListView \_ enablegroupview**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)aufrufen.

Eine Gruppe kann nicht in ein leeres Listenansicht-Steuerelement eingefügt werden.

Stellen Sie sicher, dass die **igroupid** in den Elementen festgelegt ist, der die Gruppe hinzugefügt wurde. Andernfalls zeigt das ListView-Steuerelement nach der [**LVM- \_ enablegroupview**](lvm-enablegroupview.md) -Nachrichtenverarbeitung mit **true** keine Elemente an.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, in dem die Comclt32-Version 6,0 angegeben wird. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





