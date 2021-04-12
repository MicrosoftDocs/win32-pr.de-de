---
title: LVM_GETFOOTERITEMRECT Meldung (kommstrg. h)
description: Ruft die Koordinaten einer Fußzeile für ein angegebenes Element in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooteritemrect-Makros.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERITEMRECT Meldung
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
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213702"
---
# <a name="lvm_getfooteritemrect-message"></a>LVM \_ getfooteritemrect-Meldung

Ruft die Koordinaten einer Fußzeile für ein angegebenes Element in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooteritemrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der Index des Elements im Listenansicht-Steuerelement.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten empfängt. Die aufrufenden Anwendung ist für die Zuordnung dieser Struktur verantwortlich. Die empfangenen Koordinaten werden als Client Koordinaten ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

