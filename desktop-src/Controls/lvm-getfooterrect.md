---
title: LVM_GETFOOTERRECT Meldung (kommstrg. h)
description: Ruft die Koordinaten der Fußzeile für ein Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooterrect-Makros.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERRECT Meldung
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
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102894"
---
# <a name="lvm_getfooterrect-message"></a>LVM- \_ getfooterrect-Nachricht

Ruft die Koordinaten der Fußzeile für ein Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooterrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet. Muss den Wert 0 (null) haben.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten empfängt. Der Aufrufprozess ist für die Zuordnung dieser Struktur verantwortlich. Die empfangenen Koordinaten werden als Client Koordinaten ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

