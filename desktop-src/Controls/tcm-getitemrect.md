---
title: TCM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für eine Registerkarte in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetItemRect-Makros senden.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- Windows-Steuerelemente für TCM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859198"
---
# <a name="tcm_getitemrect-message"></a>TCM \_ GetItemRect-Nachricht

Ruft das umgebende Rechteck für eine Registerkarte in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck der Registerkarte in viewportkoordinaten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

