---
title: LVM_SETTEXTBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe von Text in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ settextbkcolor-Makros senden.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Windows-Steuerelemente für LVM_SETTEXTBKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040440"
---
# <a name="lvm_settextbkcolor-message"></a>LVM- \_ settextbkcolor-Meldung

Legt die Hintergrundfarbe von Text in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ settextbkcolor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Text Hintergrundfarbe. Dies kann CLR none sein, \_ Wenn keine Hintergrundfarbe angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





