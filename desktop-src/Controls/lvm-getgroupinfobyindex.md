---
title: LVM_GETGROUPINFOBYINDEX (Commctrl.h)
description: Ruft Informationen zu einer angegebenen Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des \_ ListView-Makros GetGroupInfoByIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482683e9d1026c1deed17bf1f05310d63ac2127a6a2a6f32b5b5d95a0fbbea3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877400"
---
# <a name="lvm_getgroupinfobyindex-message"></a>LVM \_ GETGROUPINFOBYINDEX-Nachricht

Ruft Informationen zu einer angegebenen Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros GetGroupInfoByIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der Index der Gruppe.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**LVGROUP-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) um Informationen zu der durch *wParam* angegebenen Gruppe zu empfangen. Der aufrufende Prozess ist für die Zuweisung von Arbeitsspeicher für die Struktur und alle Puffer in der Struktur verantwortlich, z. B. den Puffer, auf den der **pszHeader-Member zeigt.** Legen Sie alle abhängigen Member der -Struktur fest, z. B. **cchHeader** die Größe des Puffers, auf den **pszHeader** in **WCHARs** zeigt, einschließlich des beendenden **NULL-Werts.** Legen **Sie cbSize** auf sizeof(LVGROUP) fest.

Der Nachrichtenempfänger ist dafür verantwortlich, die Strukturmitglieder mit Informationen für die durch *wParam* angegebene Gruppe festzulegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





