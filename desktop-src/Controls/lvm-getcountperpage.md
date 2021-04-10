---
title: LVM_GETCOUNTPERPAGE Meldung (kommstrg. h)
description: Berechnet die Anzahl der Elemente, die vertikal in den sichtbaren Bereich eines Listenansicht-Steuer Elements passen, wenn Sie in der Listen-oder Berichtsansicht enthalten sind. Nur vollständig sichtbare Elemente werden gezählt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getzähltperpage-Makros senden.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Windows-Steuerelemente für LVM_GETCOUNTPERPAGE Meldung
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
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040106"
---
# <a name="lvm_getcountperpage-message"></a>LVM \_ getgräfin-Nachricht

Berechnet die Anzahl der Elemente, die vertikal in den sichtbaren Bereich eines Listenansicht-Steuer Elements passen, wenn Sie in der Listen-oder Berichtsansicht enthalten sind. Nur vollständig sichtbare Elemente werden gezählt. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getzähltperpage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der vollständig sichtbaren Elemente zurück, wenn erfolgreich. Wenn die aktuelle Ansicht eine Symbol-oder kleine Symbol Ansicht ist, ist der Rückgabewert die Gesamtzahl der Elemente im Listenansicht-Steuerelement.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





