---
title: TVM_GETSCROLLTIME Meldung (kommstrg. h)
description: Ruft die maximale Scrollzeit für das Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ getscrolltime-Makros senden.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Windows-Steuerelemente für TVM_GETSCROLLTIME Meldung
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103210"
---
# <a name="tvm_getscrolltime-message"></a>TVM \_ getscrolltime-Meldung

Ruft die maximale Scrollzeit für das Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ getscrolltime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die maximale Scrollzeit in Millisekunden zurück.

## <a name="remarks"></a>Bemerkungen

Die maximale Scrollzeit ist die längste Zeitspanne, die ein scrollvorgang ausführen kann. Der Bildlauf wird so angepasst, dass der Bildlauf innerhalb der maximalen Scrollzeit stattfindet. Ein scrollvorgang kann weniger Zeit in Anspruch nehmen als das Maximum.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ setscrolltime**](tvm-setscrolltime.md)
</dt> </dl>

 

 





