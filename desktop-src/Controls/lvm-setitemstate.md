---
title: LVM_SETITEMSTATE (Commctrl.h)
description: Ändert den Zustand eines Elements in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetItemState-Makros senden.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b7375ad7edb32459fe6029081ec0a872d3673c90003e34ca21cd795d3a79ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217415"
---
# <a name="lvm_setitemstate-message"></a>LVM \_ SETITEMSTATE-Meldung

Ändert den Zustand eines Elements in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetItemState-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Listenansichtselements. Wenn dieser Parameter -1 ist, wird die Zustandsänderung auf alle Elemente angewendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Das **stateMask-Element** gibt an, welche  Zustandsbits geändert werden müssen, und das Zustandsmitglied enthält die neuen Werte für diese Bits. Die anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie diese Nachricht explizit senden, wird **TRUE** zurückgegeben, wenn sie erfolgreich war, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Der Zustandswert eines Elements enthält einen Satz von Bitflags, die den Zustand des Elements angeben. Der Zustandswert kann auch Bildlistenindizes enthalten, die das Statusbild und das Überlagerungsbild des Elements angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





