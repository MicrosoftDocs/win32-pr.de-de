---
title: TVM_SETHOT Meldung (kommstrg. h)
description: Legt das heiße Element für ein Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView-Makros "-Host" senden \_ .
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Windows-Steuerelemente für TVM_SETHOT Meldung
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
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957036"
---
# <a name="tvm_sethot-message"></a>TVM- \_ Nachricht

\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]

Legt das heiße Element für ein Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) -Makros "-Host" senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das neue heiße Element. Wenn dieser Wert **null** ist, wird für das Strukturansicht-Steuerelement festgelegt, dass kein heißes Element vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.

## <a name="remarks"></a>Bemerkungen

Das *heiße Element* ist das Element, auf das der Mauszeiger zeigt. Mit dieser Meldung wird ein Element so aussehen, als wäre es das heiße Element, auch wenn der Mauszeiger nicht darauf zeigt.

Diese Meldung hat keinen sichtbaren Effekt, wenn der Stil für die [**TV- \_ trackselect**](tree-view-control-window-styles.md) -Einstellung nicht festgelegt ist

Wenn dies erfolgreich ist, bewirkt diese Meldung, dass das heiße Element neu gezeichnet wird.

Diese Meldung wird ignoriert, wenn *LPARAM* den Wert **null** hat und das Strukturansicht-Steuerelement die Maus nachverfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TreeView \_ -Element**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





