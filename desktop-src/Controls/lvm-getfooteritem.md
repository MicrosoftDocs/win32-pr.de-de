---
title: LVM_GETFOOTERITEM Meldung (kommstrg. h)
description: Ruft Informationen zu einem footerelement in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooteritem-Makros.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERITEM Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040100"
---
# <a name="lvm_getfooteritem-message"></a>LVM- \_ getfooteritem-Nachricht

Ruft Informationen zu einem footerelement in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooteritem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der Index des Elements.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine " [**lvfooteritem**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) "-Struktur, die einen Wert für den **Zustand** und/oder **pszText** -Member gemäß dem Wert des **Masken** Members empfängt. Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und deren Member festzulegen, um dem Empfänger anzugeben, welche Informationen zurückgegeben werden sollen. Weitere Informationen finden Sie unter " **lvfooteritem**".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





