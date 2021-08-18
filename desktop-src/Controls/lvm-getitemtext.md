---
title: LVM_GETITEMTEXT Meldung (Commctrl.h)
description: Ruft den Text eines Listenansichtselements oder -unterelements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemText-Makros senden.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d5292f9814b3ef62667d44582eab44a2f18ac6c274682d180dd26f1b7cdd9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062580"
---
# <a name="lvm_getitemtext-message"></a>LVM \_ GETITEMTEXT-Nachricht

Ruft den Text eines Listenansichtselements oder -unterelements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemText-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Listenansichtselements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Legen Sie **iSubItem** auf 0 (null) fest, um den Elementtext abzurufen. Legen Sie **iSubItem** auf den Index des Unteritems fest, um den Text eines Unteritems abzurufen. Der **pszText-Member** zeigt auf einen Puffer, der den Text empfängt. Das **cchTextMax-Element** gibt die Anzahl der Zeichen im Puffer an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie diese Nachricht explizit senden, wird die Anzahl der Zeichen im **pszText-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) zurückgegeben.

## <a name="remarks"></a>Hinweise

Sie können diese Nachricht auch senden, indem Sie das [**ListView \_ GetItemText-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) aufrufen. Dieses Makro gibt jedoch nicht die Zeichenfolgenlänge zurück.

**LVM \_ GETITEMTEXT** wird im [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) und **LVM \_ GETITEMTEXTA** (ANSI)<br/>           |



 

 





