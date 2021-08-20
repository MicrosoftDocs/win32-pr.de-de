---
title: LVM_GETFOOTERITEMRECT Meldung (Commctrl.h)
description: Ruft die Koordinaten einer Fußzeile für ein angegebenes Element in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetFooterItemRect-Makros.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5df635c18de3dec7cad128fe23ceeea2829b273984c561f5f289e2f0533b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830671"
---
# <a name="lvm_getfooteritemrect-message"></a>LVM \_ GETFOOTERITEMRECT-Nachricht

Ruft die Koordinaten einer Fußzeile für ein angegebenes Element in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetFooterItemRect-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der Index des Elements im Listenansicht-Steuerelement.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um die Koordinaten zu empfangen. Die aufrufende Anwendung ist für die Zuordnung dieser Struktur verantwortlich. Die empfangenen Koordinaten werden als Clientkoordinaten ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

