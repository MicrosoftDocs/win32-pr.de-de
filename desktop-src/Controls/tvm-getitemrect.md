---
title: TVM_GETITEMRECT (Commctrl.h)
description: Ruft das umgebundene Rechteck für ein Strukturansichtselement ab und gibt an, ob das Element sichtbar ist. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemRect-Makros senden.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT von Windows-Steuerelementen
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
ms.openlocfilehash: 1c6b58ff7d2ce88fd4257ce7db84fa8bd9b4fa2b2d223af03a3f1d57a83c9b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054000"
---
# <a name="tvm_getitemrect-message"></a>TVM \_ GETITEMRECT-Nachricht

Ruft das umgebundene Rechteck für ein Strukturansichtselement ab und gibt an, ob das Element sichtbar ist. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemRect-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der den Teil des Elements angibt, für den das umgebundene Rechteck abgerufen werden soll. Wenn dieser Parameter **TRUE ist,** enthält das umgebundene Rechteck nur den Text des Elements. Andernfalls enthält sie die gesamte Zeile, die das Element im Strukturansicht-Steuerelement einnimmt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die beim Senden der Nachricht das Handle des Elements enthält, für das das Rechteck abgerufen werden soll. Weitere Informationen zum Platzieren des Elementhandpunkts in diesem Parameter finden Sie im folgenden Beispiel. Nach der Rückgabe aus der Nachricht enthält dieser Parameter das umgebundene Rechteck. Die Koordinaten sind relativ zur oberen linken Ecke des Strukturansicht-Steuerelements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Element sichtbar ist und das umgebundene Rechteck erfolgreich abgerufen wurde, ist der Rückgabewert **TRUE.** Andernfalls gibt die Meldung **FALSE zurück** und ruft das umgebundene Rechteck nicht ab.

## <a name="remarks"></a>Hinweise

Beim Senden dieser Nachricht enthält *der lParam-Parameter* das Handle des Elements, für das das Rechteck abgerufen wird. Das Handle wird in *lParam platziert,* wie im folgenden Beispiel gezeigt:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

