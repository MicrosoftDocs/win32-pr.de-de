---
title: TVM_GETITEMSTATE Meldung (kommstrg. h)
description: Ruft einige oder alle Zustands Attribute eines Struktur Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemState-Makros senden.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Windows-Steuerelemente für TVM_GETITEMSTATE Meldung
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
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040788"
---
# <a name="tvm_getitemstate-message"></a>TVM- \_ GetItemState-Meldung

Ruft einige oder alle Zustands Attribute eines Struktur Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Element.

</dd> <dt>

*lParam* 
</dt> <dd>

Maske, die verwendet wird, um die abzufragende Zustände anzugeben. Dies entspricht dem **Status Ask** -Member von [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **uint** -Wert zurück, bei dem die entsprechenden Zustands Bits auf **true** festgelegt sind. Nur die Bits, die von *LPARAM* angegeben werden und **true** sind, werden festgelegt. Dieser Wert entspricht dem **State** -Member von [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





