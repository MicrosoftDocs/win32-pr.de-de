---
title: TVM_GETITEMSTATE (Commctrl.h)
description: Ruft einige oder alle Zustandsattribute eines Strukturansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemState-Makros senden.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE message Windows Controls
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff562af5a97684caa3e5b17ab47d0f67f82a6789e2510cf1598a3189073fda81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261260"
---
# <a name="tvm_getitemstate-message"></a>TVM \_ GETITEMSTATE-Nachricht

Ruft einige oder alle Zustandsattribute eines Strukturansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemState-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Element.

</dd> <dt>

*lParam* 
</dt> <dd>

Maske, die verwendet wird, um die zu abfragenden Zustände anzugeben. Sie entspricht dem **stateMask-Member** von [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **UINT-Wert** zurück, bei dem die entsprechenden Zustandsbits auf **TRUE festgelegt sind.** Es werden nur die Bits festgelegt, die *von lParam angegeben* werden und **TRUE** sind. Dieser Wert entspricht dem **Zustandsmitglied** [**von TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





