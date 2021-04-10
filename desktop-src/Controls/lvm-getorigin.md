---
title: LVM_GETORIGIN Meldung (kommstrg. h)
description: Ruft den aktuellen Ansichts Ursprung für ein Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getorigin-Makros senden.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Windows-Steuerelemente für LVM_GETORIGIN Meldung
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
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105495"
---
# <a name="lvm_getorigin-message"></a>LVM \_ getorigin-Nachricht

Ruft den aktuellen Ansichts Ursprung für ein Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getorigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die den Ansichts Ursprung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn die aktuelle Ansicht eine Listen-oder Berichtsansicht ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

