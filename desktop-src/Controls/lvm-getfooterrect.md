---
title: LVM_GETFOOTERRECT-Nachricht (Commctrl.h)
description: Ruft die Koordinaten der Fußzeile für ein Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetFooterRect-Makros.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bc2c5cd724c9b5b4885b99123489e49ead52243d43388e7eb22808fb43a826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411459"
---
# <a name="lvm_getfooterrect-message"></a>LVM \_ GETFOOTERRECT-Nachricht

Ruft die Koordinaten der Fußzeile für ein Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetFooterRect-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet. Muss den Wert 0 (null) haben.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um die Koordinaten zu empfangen. Der aufrufende Prozess ist für die Zuordnung dieser Struktur verantwortlich. Die empfangenen Koordinaten werden als Clientkoordinaten ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

