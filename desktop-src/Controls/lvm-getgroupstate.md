---
title: LVM_GETGROUPSTATE Meldung (kommstrg. h)
description: Ruft den Zustand für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getgroupstate-Makros.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Windows-Steuerelemente für LVM_GETGROUPSTATE Meldung
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
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475375"
---
# <a name="lvm_getgroupstate-message"></a>LVM \_ getgroupstate-Meldung

Ruft den Zustand für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getgroupstate**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt die Group by **igroupid** an (siehe Struktur von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ").

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Gibt die abzurufenden Zustands Werte an. Dies ist eine Kombination der Flags, die für das **State** -Mitglied von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)" aufgelistet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Kombination von Zustands Werten zurück, die festgelegt werden. Wenn z. b. *LPARAM* auf "lvgs reduziert" \_ und der zurückgegebene Wert 0 (null) ist, wird der reduzierte Status der Netzwerk Sicherheitsgruppen \_ nicht festgelegt NULL wird zurückgegeben, wenn die Gruppe nicht gefunden wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





