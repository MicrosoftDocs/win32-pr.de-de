---
title: LVM_GETGROUPSTATE Nachricht (Commctrl.h)
description: Ruft den Zustand für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetGroupState-Makros.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66272dd259e80f239804ffadbd706370f948a2505173cc03aaa40057b273a629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958429"
---
# <a name="lvm_getgroupstate-message"></a>LVM \_ GETGROUPSTATE-Nachricht

Ruft den Zustand für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetGroupState-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt die Gruppe nach **iGroupId** an (siehe [**LVGROUP-Struktur).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Gibt die abzurufenden Zustandswerte an. Dies ist eine Kombination der Flags, die für den **Statusmember** von [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)aufgelistet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Kombination der festgelegten Zustandswerte zurück. Wenn *lParam* beispielsweise LVGS COLLAPSED ist \_ und der zurückgegebene Wert 0 (null) ist, wird der \_ LVGS COLLAPSED-Zustand nicht festgelegt. 0 (null) wird zurückgegeben, wenn die Gruppe nicht gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





