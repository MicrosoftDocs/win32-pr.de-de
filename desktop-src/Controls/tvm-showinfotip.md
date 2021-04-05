---
title: TVM_SHOWINFOTIP Meldung (kommstrg. h)
description: Zeigt den Infotipp für ein angegebenes Element in einem Strukturansicht-Steuerelement an. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ ShowInfoTip-Makros senden.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Windows-Steuerelemente für TVM_SHOWINFOTIP Meldung
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859289"
---
# <a name="tvm_showinfotip-message"></a>TVM \_ ShowInfoTip-Meldung

Zeigt den Infotipp für ein angegebenes Element in einem Strukturansicht-Steuerelement an. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Handle für das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Von den meisten Anwendungen wird diese Nachricht nicht verwendet. Infotips werden automatisch angezeigt. Weitere Informationen finden Sie unter Verwenden von Strukturansicht-Infotipps in der Übersicht [über Tree-View](tree-view-controls.md) -Steuerelemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





