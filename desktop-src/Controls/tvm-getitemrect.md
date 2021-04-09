---
title: TVM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für ein Struktur Ansichts Element ab und gibt an, ob das Element sichtbar ist. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemRect-Makros senden.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Windows-Steuerelemente für TVM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103462"
---
# <a name="tvm_getitemrect-message"></a>TVM- \_ GetItemRect-Meldung

Ruft das umgebende Rechteck für ein Struktur Ansichts Element ab und gibt an, ob das Element sichtbar ist. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein-Wert, der den Teil des Elements angibt, für den das umgebende Rechteck abgerufen werden soll. Wenn dieser Parameter **true** ist, enthält das umgebende Rechteck nur den Text des Elements. Andernfalls enthält Sie die gesamte Zeile, die das Element im Strukturansicht-Steuerelement einnimmt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die beim Senden der Nachricht das Handle des Elements enthält, für das das Rechteck abgerufen werden soll. Im folgenden Beispiel finden Sie weitere Informationen dazu, wie Sie das Element Handle in diesem Parameter platzieren. Nachdem die Nachricht zurückgegeben wurde, enthält dieser Parameter das umgebende Rechteck. Die Koordinaten sind relativ zur linken oberen Ecke des Strukturansicht-Steuer Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Element sichtbar ist und das umgebende Rechteck erfolgreich abgerufen wurde, ist der Rückgabewert " **true**". Andernfalls gibt die Nachricht **false** zurück und ruft das umgebende Rechteck nicht ab.

## <a name="remarks"></a>Bemerkungen

Beim Senden dieser Nachricht enthält der *LPARAM* -Parameter das Handle des Elements, für das das Rechteck abgerufen wird. Das Handle wird in *LPARAM* platziert, wie im folgenden Beispiel gezeigt:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

