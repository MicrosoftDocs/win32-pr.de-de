---
title: LVM_GETCOLUMNWIDTH (Commctrl.h)
description: Ruft die Breite einer Spalte in der Berichts- oder Listenansicht ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetColumnWidth-Makros senden.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH message Windows Controls
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800ab7172ec489b84506cc55a342325527f38e447fc2bae635c2e5688a142b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411506"
---
# <a name="lvm_getcolumnwidth-message"></a>LVM \_ GETCOLUMNWIDTH-Nachricht

Ruft die Breite einer Spalte in der Berichts- oder Listenansicht ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetColumnWidth-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der Spalte. Dieser Parameter wird in der Listenansicht ignoriert.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Spaltenbreite zurück, wenn erfolgreich, andernfalls 0 (null). Wenn diese Meldung an ein Listenansicht-Steuerelement mit dem [**LVS \_**](list-view-window-styles.md) REPORT-Format gesendet wird und die angegebene Spalte nicht vorhanden ist, ist der Rückgabewert nicht definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





