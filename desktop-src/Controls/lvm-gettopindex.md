---
title: LVM_GETTOPINDEX Meldung (kommstrg. h)
description: Ruft den Index des obersten sichtbaren Elements ab, wenn es sich in der Liste oder in der Berichtsansicht handelt. Sie können diese Nachricht explizit oder mit dem ListView \_ gettopindex-Makro senden.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Windows-Steuerelemente für LVM_GETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340360"
---
# <a name="lvm_gettopindex-message"></a>LVM \_ gettopindex-Meldung

Ruft den Index des obersten sichtbaren Elements ab, wenn es sich in der Liste oder in der Berichtsansicht handelt. Sie können diese Nachricht explizit oder mit dem [**ListView \_ gettopindex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, wenn erfolgreich. Gibt 0 (null) zurück, wenn das Listenansicht-Steuerelement in der Symbol Ansicht oder in der kleinen Symbol Ansicht angezeigt wird, oder wenn sich das Listenansicht-Steuerelement in der Detailansicht befindet

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





