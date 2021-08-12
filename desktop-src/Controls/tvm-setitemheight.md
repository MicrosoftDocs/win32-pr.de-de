---
title: TVM_SETITEMHEIGHT Meldung (Commctrl.h)
description: Legt die Höhe der Strukturansichtselemente fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetItemHeight-Makros senden.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afff57188a9683d18c6bff780b4a9f61479526d44ea77985742520a47e66cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669645"
---
# <a name="tvm_setitemheight-message"></a>TVM \_ SETITEMHEIGHT-Nachricht

Legt die Höhe der Strukturansichtselemente fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetItemHeight-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neue Höhe jedes Elements in der Strukturansicht in Pixel. Die Höhe kleiner als 1 wird auf 1 festgelegt. Wenn dieses Argument nicht gerade ist und das Strukturansichtssteuerelement nicht den [**TVS \_ NONEVENHEIGHT-Stil**](tree-view-control-window-styles.md) auf besitzt, wird dieser Wert auf den nächsten geraden Wert abgerundet. Wenn dieses Argument -1 ist, wird das Steuerelement mit seiner Standardelementhöhe auf zurückgesetzt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Höhe der Elemente in Pixel zurück.

## <a name="remarks"></a>Hinweise

Das Strukturansichtssteuerelement verwendet diesen Wert für die Höhe aller Elemente. Informationen zum Ändern der Höhe einzelner Elemente finden Sie in der Beschreibung des **iIntegral-Elements** der [**TVITEMEX-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





