---
title: LVM_GETORIGIN Meldung (Commctrl.h)
description: Ruft den aktuellen Ansichtsursprung für ein Listenansichtssteuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetOrigin-Makros senden.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411357"
---
# <a name="lvm_getorigin-message"></a>LVM \_ GETORIGIN-Nachricht

Ruft den aktuellen Ansichtsursprung für ein Listenansichtssteuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetOrigin-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**POINT-Struktur,**](/previous-versions//dd162805(v=vs.85)) die den Ansichtsursprung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn es sich bei der aktuellen Ansicht um eine Listen- oder Berichtsansicht handelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

