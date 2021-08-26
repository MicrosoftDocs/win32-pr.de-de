---
title: LVM_GETCOUNTPERPAGE Meldung (Commctrl.h)
description: Berechnet die Anzahl der Elemente, die vertikal in den sichtbaren Bereich eines Listenansichtssteuerelements passen können, wenn sie sich in der Listen- oder Berichtsansicht befinden. Es werden nur vollständig sichtbare Elemente gezählt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetCountPerPage-Makros senden.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb5e7acf0c3db4add2d986a1821b9a76ae30fc1aec0af369e48e35e2a424f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968340"
---
# <a name="lvm_getcountperpage-message"></a>LVM \_ GETCOUNTPERPAGE-Nachricht

Berechnet die Anzahl der Elemente, die vertikal in den sichtbaren Bereich eines Listenansichtssteuerelements passen können, wenn sie sich in der Listen- oder Berichtsansicht befinden. Es werden nur vollständig sichtbare Elemente gezählt. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetCountPerPage-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Anzahl der vollständig sichtbaren Elemente zurück. Wenn es sich bei der aktuellen Ansicht um ein Symbol oder eine kleine Symbolansicht handelt, ist der Rückgabewert die Gesamtzahl der Elemente im Listenansicht-Steuerelement.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





