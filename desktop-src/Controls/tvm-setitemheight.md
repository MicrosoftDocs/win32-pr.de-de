---
title: TVM_SETITEMHEIGHT Meldung (kommstrg. h)
description: Legt die Höhe der Elemente in der Strukturansicht fest. Sie können diese Nachricht explizit oder mithilfe des TreeView-Objekts " \_ abtitemheight" senden.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Windows-Steuerelemente für TVM_SETITEMHEIGHT Meldung
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
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956630"
---
# <a name="tvm_setitemheight-message"></a>TVM-Meldung "". \_

Legt die Höhe der Elemente in der Strukturansicht fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Objekts " \_ abtitemheight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die neue Höhe jedes Elements in der Strukturansicht in Pixel. Höhen, die kleiner als 1 sind, werden auf 1 festgelegt. Wenn dieses Argument nicht gerade ist und das Strukturansicht-Steuerelement nicht über den nicht- [**\_ evenheight**](tree-view-control-window-styles.md) -Stil des Fernseh Baums verfügt, wird dieser Wert auf den nächstgelegenen geraden Wert gerundet. Wenn dieses Argument-1 ist, wird das Steuerelement auf seine Standardelement Höhe zurückgesetzt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Höhe der Elemente in Pixel zurück.

## <a name="remarks"></a>Bemerkungen

Das Strukturansicht-Steuerelement verwendet diesen Wert für die Höhe aller Elemente. Informationen zum Ändern der Höhe einzelner Elemente finden Sie in der Beschreibung des **iintegral** -Members der [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GetItemHeight**](tvm-getitemheight.md)
</dt> </dl>

 

 





