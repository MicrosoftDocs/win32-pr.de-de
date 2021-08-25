---
title: LVM_GETTOPINDEX-Nachricht (Commctrl.h)
description: Ruft den Index des am höchsten sichtbaren Elements ab, wenn es sich in der Listen- oder Berichtsansicht befindet. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetTopIndex-Makros senden.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920040"
---
# <a name="lvm_gettopindex-message"></a>LVM \_ GETTOPINDEX-Nachricht

Ruft den Index des am höchsten sichtbaren Elements ab, wenn es sich in der Listen- oder Berichtsansicht befindet. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetTopIndex-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index des Elements zurück. Gibt 0 (null) zurück, wenn sich das Listenansichts-Steuerelement in der Symbolansicht oder kleinen Symbolansicht befindet oder wenn sich das Listenansichts-Steuerelement in der Detailansicht mit aktivierten Gruppen befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





