---
title: TVM_SETHOT Nachricht (Commctrl.h)
description: Legt das heiße Element für ein Strukturansichtssteuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetHot-Makros senden.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ca61fd0bd3e25f37229cd5cee54f9bbb59b3a5c7556ae745821a8dc4d595d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913950"
---
# <a name="tvm_sethot-message"></a>TVM \_ SETHOT-Nachricht

\[Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird in zukünftigen Versionen von Windows möglicherweise nicht mehr unterstützt.\]

Legt das heiße Element für ein Strukturansichtssteuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetHot-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das neue heiße Element. Wenn dieser Wert **NULL** ist, wird das Strukturansichtssteuerelement auf kein heißes Element festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden.

## <a name="remarks"></a>Hinweise

Das *heiße Element* ist das Element, auf das die Maus zeigen soll. Diese Meldung bewirkt, dass ein Element so aussieht, als wäre es das heiße Element, auch wenn die Maus nicht darauf zeigen würde.

Diese Meldung hat keine sichtbaren Auswirkungen, wenn der [**TVS \_ TRACKSELECT-Stil**](tree-view-control-window-styles.md) nicht festgelegt ist.

Wenn dies erfolgreich ist, bewirkt diese Meldung, dass das heiße Element neu gezeichnet wird.

Diese Meldung wird ignoriert, wenn *lParam* **NULL** ist und das Strukturansichtssteuerelement die Maus nachverfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





