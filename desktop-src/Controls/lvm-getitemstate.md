---
title: LVM_GETITEMSTATE (Commctrl.h)
description: Ruft den Status eines Listenansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemState-Makros senden.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4737be14f3e975f87a6cbea460ef53dd40ecbb7b6a2d06c39a247dbe8aa0a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958299"
---
# <a name="lvm_getitemstate-message"></a>LVM \_ GETITEMSTATE-Nachricht

Ruft den Status eines Listenansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemState-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Listenansichtselements.

</dd> <dt>

*lParam* 
</dt> <dd>

Abzurufende Zustandsinformationen. Dieser Parameter kann eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                                                           | Bedeutung                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | Das Element ist für einen Ausschneide- und Einfügevorgang markiert.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel hervorgehoben.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**\_LVIS-FOKUS**</dt> </dl>                      | Das Element hat den Fokus, sodass es von einem Standardfokusrechteck umgeben ist. Obwohl mehr als ein Element ausgewählt werden kann, kann nur ein Element den Fokus haben.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECTED**</dt> </dl>                   | Das Element ist ausgewählt. Die Darstellung eines ausgewählten Elements hängt davon ab, ob es den Fokus besitzt, und auch von den Systemfarben, die für die Auswahl verwendet werden.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Verwenden Sie diese Maske, um den Überlagerungsbildindex des Elements abzurufen.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Verwenden Sie diese Maske, um den Statusbildindex des Elements abzurufen.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den aktuellen Zustand für das angegebene Element zurück. Die einzigen gültigen Bits im Rückgabewert sind die Bits, die den im *lParam-Parameter festgelegten Bits* entsprechen.

## <a name="remarks"></a>Hinweise

Die Zustandsinformationen eines Elements enthalten eine Reihe von Bitflags sowie Bildlistenindizes, die das Statusbild und das Überlagerungsbild des Elements angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)
</dt> </dl>

 

 





